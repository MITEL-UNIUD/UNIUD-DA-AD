# UNIUD-DA-AD
UNIUD Daily Activities Accelerometer Dataset

The present dataset has been developed to experiment with techniques for recognizing activities of daily living (ADL) with different intensity, using a smartphone with an app for recording accelerometer data.
10 subjects repeated a series of activities for 3 times, each time with the smartphone in a different position (arm, pocket, wrist). 
Activities were selected in order to represent different household activity levels according to their MET: sitting (1 MET), sitting and working at the computer (1.8 MET), walking (2 MET), ironing (2.3 MET), sweeping the floor (3.3 MET), going down stairs with a shopping bag (5 MET), walking while carrying a large box (6 MET), and climbing stairs with a shopping bag (7.5 MET). Each activity lasted 30 seconds, for a total of 12 minutes/subject.
A total of 117714 samples have been recorded. 

Data are provided in three CSV files, named after the smartphone position, with the following structure:

```subject,position,activity,segment,sample,ms,x_acc,y_acc,z_acc```

with the following meaning:
- `subject`: 1...10. Age and sex are provided in a separate file;
- `position`: arm/pocket/wrist;
- `activity`: climbing_stairs/ computer/ down_stairs/ ironing/ sitting/ sweeping/ walking/ walking_box. In addition, a "removed" label indicates segments that, being of transition, did not represent specifically one activity. The tail of the samples for each user, a total of few seconds after the activities, is not labeled. Finally, in the "sitting" activity, not always the subjects were motionless.
- `segment`: in the original work we segmented data in 5 seconds segments, on which we calculated features. These are identified also in data, for the sake of completeness.
- `sample`: this is just a numerical id, relative to subject and position.
- `ms`: time of acquisition, in milliseconds, from the beginning of a recording session (thus relative to subject and position);
- `x_acc`,`y_acc`,`z_acc`: acceleration on the 3 axes.


Details of the experimentation are provided in the following paper:

Vincenzo Della Mea, Omar Quattrin & Maria Parpinel (2017) *A feasibility study on smartphone accelerometer-based recognition of household activities and influence of smartphone position*, Informatics for Health and Social Care, 42:4, 321-334, DOI: 10.1080/17538157.2016.1255214
https://www.tandfonline.com/doi/full/10.1080/17538157.2016.1255214


If  you find this dataset useful, please cite the above mentioned paper.
