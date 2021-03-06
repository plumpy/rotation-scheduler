## rotation schedule extend

Extends a previously generated schedule.

### Synopsis

Once an initial schedule is in place, time will pass and that schedule
needs to be extended further into the future. During that time, users sometimes get 
added or removed from the rotation. By default, the previous scheduled shifts won't be modified.
if '--prune' is true, however, all shifts are reviewed to ensure a current member of the rotation
owns that shift. If a shift is found from a now-unknown user, shifts from that point forward are
rescheduled (regenerated) with the current rotation membership.

```
rotation schedule extend [outputFile] [flags]
```

### Options

```
  -h, --help              help for extend
  -p, --prune             Prune removes all shifts before the current shift and reschedules all shifts if shift owners are no longer in rotation.
  -s, --schedule string   Required. Filepath to the schedule to extend.
```

### Options inherited from parent commands

```
      --domains strings         Only include email addresses from --github that match these domains. A single value of '*' will allow any domain. Use '--domains []' to only use GitHub usernames. (default [*])
  -g, --github strings          Fetch the user list from GitHub. Order of args must be 'organization,team,accessToken'. Must specify an access token with read:org permissions.
  -r, --record string           Record the responses from external dependencies to the specified file. Used for external dependency testing.
  -d, --shiftDurationDays int   Optional. Duration in days for each shift. Defaults to 7, must be a positive integer. (default 7)
      --stop string             Required. Generate schedule stopping on this date (inclusive). Must be in the format 2006-01-02
  -u, --users strings           Set of users for the rotation. Required if --github* options are not specified.
```

### SEE ALSO

* [rotation schedule](rotation_schedule.md)	 - Schedule creation and extension functions.

###### Auto generated by spf13/cobra on 16-Apr-2020
