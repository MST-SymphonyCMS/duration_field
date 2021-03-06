# Duration Field

Duration field for Symphony CMS.

Allows input of duration through `duration` settings:

- weeks
- days
- hours
- minutes
- seconds
- fractions (of a second)

## Features:

- enable / disable usage of each setting. At a very minimum, `seconds` are enforced. `fractions` are allowed only with `seconds`
- sorting
- filtering

## Filters:

- Equality: `X`
- Larger: `greater than X`
- Equal or larger: `equal to or greater than X`
- Less: `less than X`
- Equal or less: `equal to or less than X`
- Range: `X to Y`

## XML result

	<duration timestamp="2044029.75">
		<weeks>3</weeks>
		<days>2</days>
		<hours>15</hours>
		<minutes>47</minutes>
		<seconds>9</seconds>
		<fractions>75</fractions>
	</duration>

## Usage in forms

1\_ Either send the timestamp:

    fields[field-handle] = 123456789.123

2\_ Or send desired `duration` settings. Any missing `duration` setting will default to 0:

	fields[field-handle][weeks] = ...
	fields[field-handle][days] = ...
	fields[field-handle][hours] = ...
	fields[field-handle][minutes] = ...
	fields[field-handle][seconds] = ...
	fields[field-handle][fractions] = ...
