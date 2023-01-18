# coffee-machine-heatmap
The file 'Data.csv' contains data related to the electricity consumption of Alexide's coffee machine.
The Date column represents the date and time of the sensor recording. Note that the dates are expressed in UTC.
To convert them to the local timezone use
df['Date'] = pd.to_datetime(df['Date'], utc = True).dt.tz_convert('Europe/Berlin')
The Energy column represents the total energy consumption, expressed in W*min (Watt minutes), starting from the sensor's activation.
Note that the sensor has been restarted several times during the observation period and, following each restart, the count is restarted from 0.
The Topic column represents the topic of the mqtt message received by the sensor.

Represent total consumption in kWh (kiloWatt hours) with a heatmap that has the x-axis as the hours of the day and the y-axis as the day of the week.
