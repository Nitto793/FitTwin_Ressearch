# Overstagnation format, version A (draft)

Overstagnation means early signs of stagnation or overtraining. It's one of the app's five targets. A different team's program works it out and writes it as its own file, so it isn't part of the forecast.

The file gives one overall answer for the whole schedule, covering all its exercises together, not one answer per exercise.

`overstagnation.versionA.json` is an example for the all-exercises schedule (`Overall_Input/all-exercises.schedule.v1.json` or `.v2.json`). Its values are made up.

```json
{
  "start_date": "2027-01-04",
  "overstagnation": {"detected": true, "risk_percent": 72}
}
```

| Field | Type | Meaning |
|---|---|---|
| `start_date` | date | Copied from the schedule, so the app can tell which schedule the file goes with. |
| `overstagnation` | object | The overall answer for the whole schedule. |
| `overstagnation.detected` | `true` or `false` | Whether the program sees early signs of stagnation or overtraining during the schedule. |
| `overstagnation.risk_percent` | whole number, 0–100 | How strong those signs are: 0 means none, 100 means certain. |

Dates and units follow the same rules as the other formats: dates are written `YYYY-MM-DD`, and the unit goes at the end of the field name.

Still open: whether `detected` simply means `risk_percent` is over some threshold, such as 50. That's for the research to decide.
