# NETS213
Final Project for NETS213

Overview of flow diagram (see Diagram&Mockups.png for actual diagram):

1. Content creation (total = 6): <br>
   (a) Select a suitable existing text RPG for comparison and pull its introduction (1) <br>
   (b) Create guidelines for content creation HIT workers (1) <br>
   (c) Create HIT (1) <br>
   (d) Implement multiple rounds of content creation HITs and approve/reject manually (3)

2. Content aggregation (total = 3): <br>
   (a) Create a Textadventures Quest account (1) <br>
   (b) Pool all content creation results into a single text RPG (2)

3. Split content (total = 2): <br>
   (a) Split text RPG into its paths (2)

4. Quality control (total = 5): <br>
   (a) Create guidelines for path improvement HIT workers (1) <br>
   (b) Create HIT (1) <br>
   (c) Implement multiple iterative rounds of path improvement HITs and approve/reject manually (3)

5. Rating comparison (total = 4): <br>
   (a) Create guidelines for rating comparison HIT workers (1) <br>
   (b) Create HIT (1) <br>
   (c) Implement parallel HITs (2)
   
Overall total: 20

Raw data: Our raw data is viewable in the "input" columns of SampleOutputQC.csv.

Quality control: Our example .csv for quality control can be viewed at SampleOutputQC.csv. The data is organized in a way such that each path is represented by text (input1), the choice (input1choice), the next text (input2), the choice (input2choice), and so on. The output is simply an edited version of the whole path. The HTML AMT HIT code for our quality control module is located in the QC file. It essentially prints out the entire path by combining the input1, input1choice, input2, input2choice, etc. columns, and then asks the worker to edit the text. The way this works is that the worker can see the whole path, but we will only ask them to edit a singular input level.

Aggregation: Our aggregation module is integrated into the quality control module, since we are using an iterative process to combine various workers' efforts into a quality text.
