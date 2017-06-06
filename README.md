# README

This is a base install of Hyrax at CUL to be used for planning and further investigation.

## Running application in **development**
1. Follow setup described in the hyrax README (https://github.com/projecthydra-labs/hyrax#getting-started). To get this running on my mac I had to install:
   - ImageMagick, ghostscript (via Homebrew)
   - FITS (https://github.com/projecthydra-labs/hyrax#characterization)
   - Redis was installed, but I had to start it via `redis-server`

2. Copy `config/secrets.template.yml` to `config/secrets.yml`

3. Add fits executable path to `config/secrets.yml`

4. Run `bundle install`
   - Note: I recommend creating a separate gemset for this project.

5. Run `rake db:migrate`

6. Start redis and leave running in background
  ```
  redis-server
  ```

7. Start rails application
   ```
   rails hydra:server
   ```

8. The administrator is currently set up to be admin@example.com. Create an account with that email in order to get admin privileges.
