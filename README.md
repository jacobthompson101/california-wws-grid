# california-wws-grid
California Wind Water Solar Grid hourly data

## docker-compose uses a Dockerfile 
Builds the Nvidia CUDA ML required packages with rapidai base image, and enables GPU ML through Docker.

Docker Jupyter notebooks at localhost:8888 

With this method the image only builds once rather than having to keep reinstalling the Python packages.
```
docker-compose up -d --build
```

### Docker volume path (change OS username path to your install path)
```
volumes:
      - "/c/Users/(username)/github/california-wws-grid:/home/rapids/notebooks/work"
```

### Caiso output parquet file
The output file below has the cleaned up hourly resampled Load MW data. To keep the filesize small I rounded to the nearest 2 decimal places.
```
caiso_oasis_14_25.parquet

Load, Solar, Wind, Net Load, Renewables, Nuclear, Large Hydro, Imports, Generation, Thermal, Load Less (Generation+Imports), hour_index
```