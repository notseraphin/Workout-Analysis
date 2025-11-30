# Workout Progress Analysis

## Overview
This project analyzes weekly training volume and 1RM progression for various muscle groups based on my raw workout logs. The goal is to identify under- or over-performing muscle groups and recommend adjustments to training volume and intensity.

## Data
- `strong_workouts.csv`: Raw workout logs from tracking app(Strong).

## Database & SQL Scripts
All SQL scripts to create and populate tables and compute analytics:

1. `1_create_tables.sql` - Creates necessary tables.  
2. `2_import_csv.sql` - Imports CSV data into tables.  
3. `3_populate_tables.sql` - Populates tables from imported data.  
4. `4_weekly_volume.sql` - Aggregates weekly sets and reps by muscle group.  
5. `5_compute_1rm_changes.sql` - Computes estimated 1RM changes per exercise.  
6. `6_progression_by_muscle.sql` - Summarizes average and total progression per muscle group.

## Results
Contains:
- Weekly set and rep totals per muscle group.  
- Average and total Δ1RM per muscle group.
Found in results.txt.

## Analysis
- Calves: Highest progression per exercise despite low volume -> current program sufficient.  
- Quads: High volume but moderate progression -> may benefit from slightly lower volume and increased intensity.  
- Triceps: Negative progression -> suggest lowering volume/increased intensity and prioritizing compound pressing movements(high frequency of extensions).  
- Biceps: Low progression -> could improve with heavier or more targeted exercises.  
- Hamstrings: Good progression -> maintain current volume and exercise selection.
- Adductors: Low progression (Note: Adductor Machine in my gym is too light, should prioritize compound leg movements for better adductor stimulus)  
- Overall: Some high-volume groups may benefit from heavier sets and progressive overload rather than further volume increases.

## How to Run
1. Create PostgreSQL database `WorkoutTimeSeries`.  
2. Run SQL scripts in order (`1_create_tables.sql` → `6_progression_by_muscle.sql`).  

