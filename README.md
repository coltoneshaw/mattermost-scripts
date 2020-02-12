# Mattermost Scripts

This repository contains a series of scripts that I have written for Mattermost to perform descrete tasks. I am sharing them here in case other Mattermost users might find them useful.

**Import Note**: This code is provided as-is without any warranty and is not sponsored, supported, or endorsed by Mattermost, Inc. Please use cautiously and test before running any of these scripts against a production server.

# SQL Queries

* **[get_all_deactivated_users.sql](get_all_deactivated_users.sql)** - This query retrieves all deactivated users in Mattermost.
* **[get_last_login_time_all_users.sql](get_last_login_time_all_users.sql)** - This query retrieves the last login time for all users in Mattermost.
* **[get_number_of_posts_in_public_private_channels.sql](get_number_of_posts_in_public_private_channels.sql)** - This query retrieves the total number of posts in the database for Public ('O') and Private ('P') channels. This includes posts that are marked as deleted or edited so the number will be larger than the total number of posts visible to users in Mattermost.
* **[get_posts_by_team_and_channel.sql](get_posts_by_team_and_channel.sql)** - The query retrieves a list of active channels by team and the total number of posts in each channel ordered by Team and Channel. This query returns only Public ('O') and Private ('P') channels and posts that are visible (not deleted or past revisions of edited posts).
* **[get_user_last_activity_at.sql](get_user_last_activity_at.sql)** - This query retrieves a list of all users and their last session activity at date and time. Important Note: If the time that the the user was last active at exceeded the configured session length in days, or the user has never logged in, the LastActivityAt field will be null.
* **[get_users_in_channels.sql](get_users_in_channels.sql)** - The following SQL query retrieves a list of active channels and the active users that are members of the channel ordered by Team, Channel, LastName and Username fields. Returns only Public ('O') and Private ('P') channels.
* **[get_users_in_teams.sql](get_users_in_teams.sql)** - The following SQL query retrieves a list of users who are membersof active teams ordered by Team, LastName, and then Username.
