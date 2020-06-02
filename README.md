# dash-117million-taxi-app
Explore 117 million taxi trips in real time with Dash and Vaex

![img](https://user-images.githubusercontent.com/1765949/83561844-d2a44300-a518-11ea-913f-6293b469df08.png)

# Running this app

Clone the repo
```
$ git clone https://github.com/vaexio/dash-117million-taxi-app
```

Run in debug mode:
```
$ python app.py
```

Run in production mode:
```
$ VAEX_NUM_THREADS=8 gunicorn -w 16 app:server -b 0.0.0.0:8050
```

## Settings
Change settings in the dash app
```
$ export TAXI_PATH=/data/taxi/yellow_taxi_2012_zones.hdf5  # change the default s3 file
$ export VAEX_NUM_THREADS=16     # change the number of threads per process/worker
$ export DASH_CACHE_TIMEOUT=240  # increase cache timeout to 4 minutes
$ export DASH_CACHE_TIMEOUT=-1  # disable cache (useful for benchmarking)
```

