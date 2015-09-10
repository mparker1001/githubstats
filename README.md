----
Description
----

This script will display commit stats for a Github user for all repos within an
organization.

----
Prerequisites
----

This was tested on PHP 5.5+. It may work on earlier versions, however.

----
Configuration
----
**Required:**
You must have a Github personal access token setup under your Github username
and this token value should be stored in an environment variable called
GITHUB_TOKEN. Visit https://github.com/settings/tokens to setup your token.

For example, once your token has been generated, add the following to your
.bash_profile file:
```
export GITHUB_TOKEN="<token_value>"
```

**Optional, but highly recommended:**
You must set the timezone or PHP timezone warnings may appear. You can set your
time zone as an environment variable called GITHUB_TIMEZONE (A list of timezones
can be found at http://php.net/manual/en/timezones.php).

For example, add the following to your .bash_profile file:
```
export GITHUB_TIMEZONE="America/Chicago"
```

----
Usage
----
Execute the "githubstats" file directly:
```
./githubstats -o <org_name> -s <start_date_in_YYYYMMDDHHMM> -e
<end_date_in_YYYYMMDDHHMM> -u <github_username> -f <file_of_github_usernames>
-d (Optional)
```

For example:
```
./githubstats -o myorg -s 201507010000 -e 201509010000 -f users.list -d
```

Another example but saving the output to a file:
```
./githubstats -o myorg -s 201507010000 -e 201509010000 -f users.list -d  >>
output.txt
```
