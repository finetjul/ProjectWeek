---
layout: pw40-project

permalink: /:path/

project_title: Visual DICOM browser
category: Infrastructure
presenter_location: In-person

key_investigators:
- name: Davide Punzo
  affiliation: Freelancer 
  country: France
  
- name: Andras Lasso
  affiliation: Perk Labs 
  country: Canada

- name: Steve Pieper
  affiliation: Isomics, Inc.
  country: USA

- name: Jean-Christophe Fillion-Robin
  affiliation: Kitware
  country: USA

- name: anyone is welcome!
  affiliation: 
  country:   
---

# Project Description
The visual DICOM browser adds query/retrieve/store capabilities for DICOM databases and visualize remote and local content with thumbnails.
The widget is the union/enhancement of 3 CTK widgets: `ctkDICOMServerSettings`, `ctkDICOMQueryRetrievePanel`, `ctkDICOMBrowser` (visualize/filter the local content).

The operations are executed by a scheduler in separate concurrent threads with a priority queue.
The current supported operations are:

- Filtering and navigation with thumbnails of local database and servers results
- Import from file system to local database.
- Query/Retrieve from servers (DIMSE `C-FIND/C-GET/C-MOVE`). All the operations are done in background and in parallel.
- Storage listener.
- Send (emits only a signal for the moment, requires external implementation).
- Remove (only from local database, not from server).
- Metadata exploration.

The widget is currently an experimental feature in Slicer (DICOM module). Current Roadmap is at [link](https://github.com/commontk/CTK/issues/1162).

Possible longer-term ENH to discuss/work during the project week:
- add data streaming from visual brower series widgets to Slicer volume nodes.
- add jobs list UI (e.g. current status, actions to stop/force retry etc..., error report per job).
- handle jobs queue in the scheduler by file (so we can restart the jobs/workers at application restart).
- implementing send (i.e. adding `ctkDICOMSendJob`, `ctkDICOMSendWorker` and `ctkDICOMSend` with underlining DIMSE `DcmStorageSCU`).
- add `DICOMweb`.

## Objective
Finalize the ctk visual DICOM browser:

1. Get feedback from users/developers. Reference: [Roadmap](https://github.com/commontk/CTK/issues/1162).
1. Discuss/start implementing the longterm ENH.

## Approach and Plan

1. Have a meeting/demo with people interested for colletting feedback.  
1. Prioritize/coordinated any future development based on the feedback.

## Progress and Next Steps

1. ...
1. ...


# Illustrations
screenshots:

<img src="https://github.com/NA-MIC/ProjectWeek/assets/7985338/38806dba-f1fa-4e71-8930-42fe7803ab2d" width="1000">
<img src="https://github.com/NA-MIC/ProjectWeek/assets/7985338/9554483b-0d56-41ea-8487-45373006880f" width="1000">

video:

<video
   autoplay muted loop
   src="https://github.com/NA-MIC/ProjectWeek/assets/7985338/599999af-f7f9-431a-b78f-a8052e285f38"
   style="width:1000px">
</video>


UML Diagram:

<img src="https://github.com/NA-MIC/ProjectWeek/assets/7985338/4e682a6d-0b8f-42be-b1b2-35e46f6018b9" width="1000">


# Background and References

[PW38 Project](https://projectweek.na-mic.org/PW38_2023_GranCanaria/Projects/SlicerVisualDICOMbrowser/)

[CTK PR1](https://github.com/commontk/CTK/pull/1142)

[CTK PR2](https://github.com/commontk/CTK/pull/1165)

[Slicer PR](https://github.com/Slicer/Slicer/pull/7525)

[Roadmap](https://github.com/commontk/CTK/issues/1162)
