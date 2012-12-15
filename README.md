KrakDroidChallenge
==================

This repository contains a KrakDroidContract.java file, which defines how to access the ContentProvider of KrakDroid Hacking Challenge application (https://play.google.com/store/apps/details?id=com.futuresimple.krakdroid).

Data models
-----------

1. DataSets - represents input data that has to be processed.
1. Solutions - groups of answers to DataSets.
1. Answers - an answer to the dataset. Answers are always grouped by Solutions.
1. Submissions - represents a submitted solution state. Synchronized with backend.

Endpoints and actions
---------------------
* /datasets (read-only)
* /solutions - insert creates a new Solution and returns it's URI (/solutions/ID)
* /solutions/ID - insert creates a new Answer to dataset DATASET_ID (required parameter) and with SOLUTION_ID set to ID from URI
* /answers (read-only)
* /submissions - insert creates a new Submission for Solution specified by SOLUTION_ID (required parameter) and *triggers data upload*

Submission process
------------------
1. Create a Solution
1. Add Answers for all DataSets to this Solution
1. Create a Submission for your Solution
