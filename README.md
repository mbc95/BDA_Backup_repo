# Visualization of provided data

Plott different Containers with different patterns.

![Visualization%20of%20provided%20data%20a4b4caf415a24716879e99263372f842/Untitled.png](Visualization%20of%20provided%20data%20a4b4caf415a24716879e99263372f842/Untitled.png)

Investigating on certain features e.g.: location, number of messurements per month, number of messurements per container:

![Visualization%20of%20provided%20data%20a4b4caf415a24716879e99263372f842/Untitled%201.png](Visualization%20of%20provided%20data%20a4b4caf415a24716879e99263372f842/Untitled%201.png)

# Preprocessing

Important steps among the preprocessing process

### Data Cleaning

Removing heigth values above 140 in order to eliminate outliers/wrong meassures

![Visualization%20of%20provided%20data%20a4b4caf415a24716879e99263372f842/Untitled%202.png](Visualization%20of%20provided%20data%20a4b4caf415a24716879e99263372f842/Untitled%202.png)

### External Data

Adding external data possibly enrichs our dataset:

- Vacation
- Rain in mm
- Outside temperature
- Holiday
- etc.

### Delta Increase instead of Height

Data contains emptying intervals and collapsing glass mounds. If our overall goal is, to predict optimal emptying intervals, it is crucial to remove such events. Therefore, we introduced "height delta" as a new feature which tells the difference between the old and new height. The events mentioned above are set to zero to avoid misspredicitons.

![Visualization%20of%20provided%20data%20a4b4caf415a24716879e99263372f842/Untitled%203.png](Visualization%20of%20provided%20data%20a4b4caf415a24716879e99263372f842/Untitled%203.png)

### Two-Track approach

Since the main issue of the provided data is fluctuation we decided to switch towards a two-track approach. Therefore, we generated a new dataset with aggregates messurements of a whole day into a single datapoint. Thus, we recieved more smoothed data.

![Visualization%20of%20provided%20data%20a4b4caf415a24716879e99263372f842/Untitled%204.png](Visualization%20of%20provided%20data%20a4b4caf415a24716879e99263372f842/Untitled%204.png)

# Modeling

In detail we developed three modeltypes:

- Linear regression
- Fully connected model
- LSTM

In the end only the LSTM contributed proper results. Nevertheless, working with these models enlighted our prospect of the provided data. Therefore, it is worth mentioning and is provided in the repository.

LSTM modell prediciton on test dataset(unseen during training):

![Visualization%20of%20provided%20data%20a4b4caf415a24716879e99263372f842/Untitled%205.png](Visualization%20of%20provided%20data%20a4b4caf415a24716879e99263372f842/Untitled%205.png)