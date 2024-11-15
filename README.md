autobrr Suite
=========

    Standalone ansible role to automate the set-up of autobrr - like autodl-irssi... but better.
      - Includes the installation of Docker (Debian-based distros) and ansible dependencies within the role.
      - Includes the option of setting up and connecting autobrr to a postgres database.
      - Includes the option of setting up omegabrr - easing the filter creation process when connected with arrs.
      - Includes the option of creating a cloudflare DNS record for your autobrr instance for reverse proxy purposes.
      - Includes the option of joining Lidarr to an existing Traefik docker network (or creating one if none exists).

Docker containers included: autobrr, omegabrr, thelounge, znc, postgres

What this role is: First and foremost, this role has been crafted and designed to serve the needs of.. me.
However, when and where possible - the role has included toggles, conditionals, and tasks to improve compatiblity and usability.
This role is intended for someone who has ansible installed and wants to deploy these apps locally or onto a remote system.

Defining 'Standalone': This role is designed to deploy the above apps and their companions and nothing more. It includes all
required defaults/variables within the role, and is designed to get these apps up and running within a single role. It is not
designed to be a one-stop OS overhaul. Those needing maximum ease, compatibility, and a large support base should try Saltbox.

Notes: 
(i) Setting up indexers/irc/filters and other config options in autobrr is done within the webui post-install
(ii) Inputting autobrr's api into omegabrr and omegabrr's api into autobrr is done post-install
(iii) You will need to input the filter id for each omegabrr client post-install.