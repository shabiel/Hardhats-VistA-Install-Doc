Ward Setup
==========

Authors: Sam Habiel. Thank you for the transcripts provided by Joanne Brougham for setting up ADT.

License: |license|

.. |license| image:: https://i.creativecommons.org/l/by/4.0/80x15.png 
   :target: http://creativecommons.org/licenses/by/4.0/ 

Last updated in May 2018.

If you have reached this point, it means that you have finished `MAS Parameter
Set-up <./SetMasParameters.html>`_.

If you have been following along, we now have three steps left.

* Create the Wards
* Create the Rooms and Beds
* Initailize the Gains and Losses System

Create Wards
------------
We are going to create two wards to correspond to the two treating specialties we
setup in the previous section: 3 West for Cardiology; 3 East for Dermatology.

Important fields:

* G&L ORDER must be filled; otherwise ADT will crash.
* HOSPITAL LOCATION FILE POINTER is silly in that you have to type the same
  exact entry again to add it to the hospital location file. Don't put a different
  entry name.
* RAI/MDS WARD must be left blank. Filling this will also cause a crash.
* The Totals field is saying "count the number of patients here and put them in
  this category". You can repeat the category in another ward, and from that
  get a total number of admitted patients within a certain category. The
  example below shows a total of "Hospital" which will count the totals for the
  hospital (both wards together). There is a total of Cardiology and a total for
  Dermatology.

From the same ``ADT System Definition`` menu, we will pick ``Ward Definition Entry/Edit``.

.. raw:: html

  <div class="code"><code>Select ADT System Definition Menu <TEST ACCOUNT> Option: <strong>WARD</strong> Definition Entry/Edit

  Select WARD LOCATION NAME: <strong>3 WEST</strong> 
   Are you adding '3 WEST' as a new WARD LOCATION (the 1ST)? No// <strong>Y</strong>  (Yes)
     WARD LOCATION HOSPITAL LOCATION FILE POINTER: <strong>3 WEST</strong> 
    Are you adding '3 WEST' as a new HOSPITAL LOCATION (the 3RD)? No// <strong>Y</strong>  (Yes)
     HOSPITAL LOCATION TYPE: <strong>W</strong>  WARD
     HOSPITAL LOCATION TYPE EXTENSION: WARD//<strong>&lt;enter&gt;</strong>
     WARD LOCATION G&L ORDER: <strong>1</strong>
  NAME: 3 WEST//<strong>&lt;enter&gt;</strong>
  PRINT WARD ON WRISTBAND: <strong>N</strong>  NO
  DIVISION: <strong>MAIN</strong> CAMPUS       999
    INSTITUTION:<strong>&lt;enter&gt;</strong>
    ABBREVIATION:<strong>&lt;enter&gt;</strong>
  BEDSECTION: <strong>MAIN</strong>
  SPECIALTY: <strong>CARDIOLOGY</strong>
  SERVICE: <strong>?</strong> 
       Enter the appropriate AMIS service for this ward location.
       Choose from:
         M        MEDICINE
         S        SURGERY
         P        PSYCHIATRY
         NH       NHCU
         NE       NEUROLOGY
         I        INTERMEDIATE MED
         R        REHAB MEDICINE
         SCI      SPINAL CORD INJURY
         D        DOMICILIARY
         B        BLIND REHAB
         NC       NON-COUNT
  SERVICE: <strong>M</strong>  MEDICINE
  PRIMARY LOCATION: <strong>3RD F</strong> 
  RAI/MDS WARD:<strong>&lt;enter&gt;</strong>
  Select AUTHORIZED BEDS DATE: <strong>T</strong>   MAY 16, 2018
    Are you adding 'MAY 16, 2018' as
      a new AUTHORIZED BEDS DATE (the 1ST for this WARD LOCATION)? No// Y  (Yes)
    NUMBER OF AUTHORIZED BEDS: <strong>5</strong>
  SERIOUSLY ILL: <strong>1</strong>  INCLUDE ON SERIOUSLY ILL LIST
  Select SYNONYM:<strong>&lt;enter&gt;</strong>
  G&L ORDER: 1//<strong>&lt;enter&gt;</strong>
  Select TOTALS: <strong>HOSPITAL</strong>
    Are you adding 'HOSPITAL' as a new TOTALS (the 1ST for this WARD LOCATION)? N
  o// <strong>Y</strong>  (Yes)
     TOTALS LEVEL: 1//<strong>&lt;enter&gt;</strong>
    PRINT IN CUMULATIVE TOTALS: <strong>Y</strong>  YES
    CUM TITLE: <strong>Hospital</strong>
  Select TOTALS: <strong>CARDIOLOGY</strong>
    Are you adding 'CARDIOLOGY' as a new TOTALS (the 2ND for this WARD LOCATION)?
   No// <strong>Y</strong>  (Yes)
     TOTALS LEVEL: 2//<strong>&lt;enter&gt;</strong>
    PRINT IN CUMULATIVE TOTALS: <strong>Y</strong>  YES
    CUM TITLE: <strong>Cardiology</strong>
  Select TOTALS:<strong>&lt;enter&gt;</strong>

  Select WARD LOCATION NAME: <strong>3 EAST</strong>
  Are you adding '3 EAST' as a new WARD LOCATION (the 2ND)? No// <strong>Y</strong>  (Yes)
     WARD LOCATION HOSPITAL LOCATION FILE POINTER: <strong>3 EAST</strong> 
    Are you adding '3 EAST' as a new HOSPITAL LOCATION (the 4TH)? No// <strong>Y</strong>  (Yes)
     HOSPITAL LOCATION TYPE: <strong>W</strong>  WARD
     HOSPITAL LOCATION TYPE EXTENSION: WARD//<strong>&lt;enter&gt;</strong>
     WARD LOCATION G&L ORDER: <strong>2</strong>
  NAME: 3 EAST//<strong>&lt;enter&gt;</strong>
  PRINT WARD ON WRISTBAND: <strong>N</strong>  NO
  DIVISION: <strong>MAIN</strong> CAMPUS     999
    INSTITUTION:<strong>&lt;enter&gt;</strong>
    ABBREVIATION:<strong>&lt;enter&gt;</strong>
  BEDSECTION: <strong>MAIN</strong>
  SPECIALTY: <strong>DERMATOLOGY</strong>
  SERVICE: <strong>M</strong>  MEDICINE
  PRIMARY LOCATION: <strong>3RD E</strong> 
  RAI/MDS WARD:<strong>&lt;enter&gt;</strong>
  Select AUTHORIZED BEDS DATE: <strong>T</strong>   MAY 16, 2018
    Are you adding 'MAY 16, 2018' as
      a new AUTHORIZED BEDS DATE (the 1ST for this WARD LOCATION)? No// Y  (Yes)
    NUMBER OF AUTHORIZED BEDS: <strong>5</strong>
  SERIOUSLY ILL: <strong>1</strong>  INCLUDE ON SERIOUSLY ILL LIST
  Select SYNONYM:<strong>&lt;enter&gt;</strong>
  G&L ORDER: 2//<strong>&lt;enter&gt;</strong>
  Select TOTALS: <strong>HOSPITAL</strong>
    Are you adding 'HOSPITAL' as a new TOTALS (the 1ST for this WARD LOCATION)? N
  o// <strong>Y</strong>   (Yes)
     TOTALS LEVEL: 1//<strong>&lt;enter&gt;</strong>
    PRINT IN CUMULATIVE TOTALS: <strong>Y</strong>  YES
    CUM TITLE: <strong>Hospital</strong>
  Select TOTALS: <strong>DERMATOLOGY</strong>
    Are you adding 'DERMATOLOGY' as a new TOTALS (the 2ND for this WARD LOCATION)
  ? No// Y  (Yes)
     TOTALS LEVEL: 2//<strong>&lt;enter&gt;</strong>
    PRINT IN CUMULATIVE TOTALS: <strong>Y</strong>  YES
    CUM TITLE: <strong>Dermatology</strong>
  Select TOTALS:<strong>&lt;enter&gt;</strong>

  Select WARD LOCATION NAME:<strong>&lt;enter&gt;</strong></code></div>

Create Room/Beds
----------------
In VistA, Rooms and Beds are a single entity. In reality, they should just be called "Beds".
A room with 3 beds may be labeled as 101-A, 101-B, and 101-C. You may add other characters to
help you designate the bed as Male/Female, Luxury vs Shared, etc.

Here we create 3 rooms in each ward. 2 of the rooms have 2 beds each; one has a
single bed for a total of 10 beds.

As explained in `VistA Initialization <./InitializeVistA.html>`_.

Same menu. Option: ``Add/Edit Beds``:

.. raw:: html

  <div class="code"><code>Select ADT System Definition Menu <TEST ACCOUNT> Option: <strong>Add/Edit Beds</strong> 

  Select ROOM-BED NAME: <strong>301-A</strong> 
    Are you adding '301-A' as a new ROOM-BED (the 1ST)? No// <strong>Y</strong>  (Yes)
  NAME: 301-A//<strong>&lt;enter&gt;</strong>
  DESCRIPTION: <strong>DOUBLE ROOM</strong>
    Are you adding 'DOUBLE ROOM' as a new ROOM-BED DESCRIPTION (the 1ST)? No// <strong>Y</strong>
    (Yes)
  Select WARD(S) WHICH CAN ASSIGN: <strong>3 WEST</strong>
    Are you adding '3 WEST' as a new WARD(S) WHICH CAN ASSIGN? No// <strong>Y</strong>  (Yes)
  Select WARD(S) WHICH CAN ASSIGN:<strong>&lt;enter&gt;</strong>

  Select ROOM-BED NAME: <strong>301-B</strong> 
    Are you adding '301-B' as a new ROOM-BED (the 2ND)? No// <strong>Y</strong>  (Yes)
  NAME: 301-B//<strong>&lt;enter&gt;</strong>
  DESCRIPTION: &lt;space bar&gt;&lt;enter&gt;   DOUBLE ROOM
  Select WARD(S) WHICH CAN ASSIGN: &lt;space bar&gt;&lt;enter&gt;   3 WEST
    Are you adding '3 WEST' as a new WARD(S) WHICH CAN ASSIGN? No// <strong>Y</strong>  (Yes)
  Select WARD(S) WHICH CAN ASSIGN:<strong>&lt;enter&gt;</strong>

  Select ROOM-BED NAME: <strong>302-A</strong> 
    Are you adding '302-A' as a new ROOM-BED (the 3RD)? No// <strong>Y</strong>  (Yes)
  NAME: 302-A//<strong>&lt;enter&gt;</strong>
  DESCRIPTION:  &lt;space bar&gt;&lt;enter&gt;  DOUBLE ROOM
  Select WARD(S) WHICH CAN ASSIGN: &lt;space bar&gt;&lt;enter&gt;   3 WEST
    Are you adding '3 WEST' as a new WARD(S) WHICH CAN ASSIGN? No// <strong>Y</strong>  (Yes)
  Select WARD(S) WHICH CAN ASSIGN:<strong>&lt;enter&gt;</strong>

  Select ROOM-BED NAME: <strong>302-B</strong> 
    Are you adding '302-B' as a new ROOM-BED (the 4TH)? No// <strong>Y</strong>  (Yes)
  NAME: 302-B//<strong>&lt;enter&gt;</strong>
  DESCRIPTION: &lt;space bar&gt;&lt;enter&gt;   DOUBLE ROOM
  Select WARD(S) WHICH CAN ASSIGN: &lt;space bar&gt;&lt;enter&gt;   3 WEST
    Are you adding '3 WEST' as a new WARD(S) WHICH CAN ASSIGN? No// <strong>Y</strong>  (Yes)
  Select WARD(S) WHICH CAN ASSIGN:<strong>&lt;enter&gt;</strong>

  Select ROOM-BED NAME: <strong>303-S</strong> 
    Are you adding '303-S' as a new ROOM-BED (the 5TH)? No// <strong>Y</strong>  (Yes)
  NAME: 303-S//<strong>&lt;enter&gt;</strong>
  DESCRIPTION: <strong>SINGLE ROOM</strong> 
    Are you adding 'SINGLE ROOM' as a new ROOM-BED DESCRIPTION (the 2ND)? No// <strong>Y</strong> 
    (Yes)
  Select WARD(S) WHICH CAN ASSIGN: &lt;space bar&gt;&lt;enter&gt;   3 WEST
    Are you adding '3 WEST' as a new WARD(S) WHICH CAN ASSIGN? No// <strong>Y</strong>  (Yes)
  Select WARD(S) WHICH CAN ASSIGN:<strong>&lt;enter&gt;</strong>

  Select ROOM-BED NAME: <strong>311-A</strong> 
    Are you adding '311-A' as a new ROOM-BED (the 6TH)? No// <strong>Y</strong>  (Yes)
  NAME: 311-A//<strong>&lt;enter&gt;</strong>
  DESCRIPTION: <strong>DOUBLE ROOM</strong> 
  Select WARD(S) WHICH CAN ASSIGN: <strong>3 EAST</strong> 
    Are you adding '3 EAST' as a new WARD(S) WHICH CAN ASSIGN? No// <strong>Y</strong>  (Yes)
  Select WARD(S) WHICH CAN ASSIGN:<strong>&lt;enter&gt;</strong>

  Select ROOM-BED NAME: <strong>311-B</strong> 
    Are you adding '311-B' as a new ROOM-BED (the 7TH)? No// <strong>Y</strong>  (Yes)
  NAME: 311-B//<strong>&lt;enter&gt;</strong>
  DESCRIPTION: &lt;space bar&gt;&lt;enter&gt;   DOUBLE ROOM 
  Select WARD(S) WHICH CAN ASSIGN: &lt;space bar&gt;&lt;enter&gt;   <strong>3 EAST</strong> 
    Are you adding '3 EAST' as a new WARD(S) WHICH CAN ASSIGN? No// <strong>Y</strong>  (Yes)
  Select WARD(S) WHICH CAN ASSIGN:<strong>&lt;enter&gt;</strong>

  Select ROOM-BED NAME: <strong>312-A</strong> 
    Are you adding '312-A' as a new ROOM-BED (the 8TH)? No// <strong>Y</strong>  (Yes)
  NAME: 312-A//<strong>&lt;enter&gt;</strong>
  DESCRIPTION: &lt;space bar&gt;&lt;enter&gt;   DOUBLE ROOM
  Select WARD(S) WHICH CAN ASSIGN: &lt;space bar&gt;&lt;enter&gt;   3 EAST
    Are you adding '3 EAST' as a new WARD(S) WHICH CAN ASSIGN? No// <strong>Y</strong>  (Yes)
  Select WARD(S) WHICH CAN ASSIGN:<strong>&lt;enter&gt;</strong>

  Select ROOM-BED NAME: <strong>312-B</strong> 
    Are you adding '312-B' as a new ROOM-BED (the 9TH)? No// <strong>Y</strong>  (Yes)
  NAME: 312-B//<strong>&lt;enter&gt;</strong>
  DESCRIPTION: &lt;space bar&gt;&lt;enter&gt;   DOUBLE ROOM
  Select WARD(S) WHICH CAN ASSIGN: &lt;space bar&gt;&lt;enter&gt;   3 EAST
    Are you adding '3 EAST' as a new WARD(S) WHICH CAN ASSIGN? No// <strong>Y</strong>  (Yes)
  Select WARD(S) WHICH CAN ASSIGN:<strong>&lt;enter&gt;</strong>

  Select ROOM-BED NAME: <strong>313-S</strong> 
    Are you adding '313-S' as a new ROOM-BED (the 10TH)? No// <strong>Y</strong>  (Yes)
  NAME: 313-S//<strong>&lt;enter&gt;</strong>
  DESCRIPTION: <strong>SINGLE ROOM</strong> 
  Select WARD(S) WHICH CAN ASSIGN: &lt;space bar&gt;&lt;enter&gt;   3 EAST
    Are you adding '3 EAST' as a new WARD(S) WHICH CAN ASSIGN? No// <strong>Y</strong>  (Yes)
  Select WARD(S) WHICH CAN ASSIGN:<strong>&lt;enter&gt;</strong></code></div>

Initialize the Gains and Losses System
--------------------------------------
Compared with the others, this is pretty easy to do. Just put zeros for all the numbers.

Same menu, option ``Gains and Losses Initialization``.


.. raw:: html

  <div class="code"><code>Select ADT System Definition Menu <TEST ACCOUNT> Option: <strong>Gains</strong>  and Losses Initialization

  05/14/2018 is the date to be initialized.


  Select WARD LOCATION NAME: <strong>3 WEST</strong> 
      PATIENTS REMAINING: <strong>0</strong>
      CUM PATIENT DAYS OF CARE: <strong>0</strong>
      CUM BED: <strong>0</strong>
      CUM DISCHARGES: <strong>0</strong>
      CUM INTER XFERS: <strong>0</strong>
      CUM PAT REMAIN: <strong>0</strong>
      CUM INTSERV XFERS: <strong>0</strong>
      CUM PASS DAYS: <strong>0</strong>
      CUM ABO DAYS: <strong>0</strong>
      CUM UA DAYS: <strong>0</strong>
      CUM 1 DAY DIALYSIS PATIENTS: <strong>0</strong>
      CUM ADMIS FROM XFER IN: <strong>0</strong>
      CUM DISCH TO  XFER OUT: <strong>0</strong>
      CUM DISCHARGES TO DEATH: <strong>0</strong>
      CUM DISCH TO 'OPT/NSC': <strong>0</strong>
      CUM ADMISSIONS: <strong>0</strong>
      ADM AFTER REHOSP >30DAYS: <strong>0</strong>
      FROM ASIH: <strong>0</strong>
      TO ASIH: <strong>0</strong>
      DISCHARGE WHILE ASIH: <strong>0</strong>
      DIED WHILE ASIH: <strong>0</strong>
      CUM INTSERV XFERS IN: <strong>0</strong>
      CUM LOSSES: <strong>0</strong>
      CUM MONTHLY PAT DAYS: <strong>0</strong>
      CUM AUTHORIZED ABSENCE: <strong>0</strong>
      CUM UNAUTHORIZED ABSENCES: <strong>0</strong>
      FEMALE PATIENTS REMAINING: <strong>0</strong>

  Select WARD LOCATION NAME: <strong>3 EAST</strong> 
      PATIENTS REMAINING: <strong>0</strong>
      CUM PATIENT DAYS OF CARE: <strong>0</strong>
      CUM BED: <strong>0</strong>
      CUM DISCHARGES: <strong>0</strong>
      CUM INTER XFERS: <strong>0</strong>
      CUM PAT REMAIN: <strong>0</strong>
      CUM INTSERV XFERS: <strong>0</strong>
      CUM PASS DAYS: <strong>0</strong>
      CUM ABO DAYS: <strong>0</strong>
      CUM UA DAYS: <strong>0</strong>
      CUM 1 DAY DIALYSIS PATIENTS: <strong>0</strong>
      CUM ADMIS FROM XFER IN: <strong>0</strong>
      CUM DISCH TO  XFER OUT: <strong>0</strong>
      CUM DISCHARGES TO DEATH: <strong>0</strong>
      CUM DISCH TO 'OPT/NSC': <strong>0</strong>
      CUM ADMISSIONS: <strong>0</strong>
      ADM AFTER REHOSP >30DAYS: <strong>0</strong>
      FROM ASIH: <strong>0</strong>
      TO ASIH: <strong>0</strong>
      DISCHARGE WHILE ASIH: <strong>0</strong>
      DIED WHILE ASIH: <strong>0</strong>
      CUM INTSERV XFERS IN: <strong>0</strong>
      CUM LOSSES: <strong>0</strong>
      CUM MONTHLY PAT DAYS: <strong>0</strong>
      CUM AUTHORIZED ABSENCE: <strong>0</strong>
      CUM UNAUTHORIZED ABSENCES: <strong>0</strong>
      FEMALE PATIENTS REMAINING: <strong>0</strong>

  Select WARD LOCATION NAME:<strong>&lt;enter&gt;</strong></code></div>

Once you are done with that, it's time to populate the Gains and Losses system for the first time.


Run the option ``Recalculate G&L Cumulative Totals``, which is located on the parent menu:

.. raw:: html

  <div class="code"><code>          Add/Edit Beds
            Bed Out-of-Service Date Enter/Edit
            Bulletin Selection
            Device Selection
            Edit Bed Control Movement Types
            Edit Ward Out-of-Service Dates
            Enter/Edit Transmission Routers File
            G&L Parameter Edit
            Gains and Losses Initialization
            MAS Parameter Entry/Edit
            Master Demographics Files ...
            Means Test Threshold Entry/Edit
            Reasons for Lodging Entry/Edit
            Template Selection
            Treating Specialty Set-up
            Ward Definition Entry/Edit

  Select ADT System Definition Menu <TEST ACCOUNT> Option:<strong>&lt;enter&gt;</strong>


            ADT System Definition Menu ...
            Check Routine Integrity
            Current MAS Release Notes
            Insurance Company Entry/Edit
            Military Service Data Inconsistencies Report
            Patient Type Update
            Purge Scheduled Admissions
            Recalculate G&L Cumulative Totals
            Reimbursable Insurance Primary EC Report
            RUG Semi-Annual Background Job
            Sharing Agreement Category Update
            Show MAS System Status Screen
            Transmit/Generate Release Comments
            Unsupported CV End Dates Report
            View G&L Corrections
            WWU Enter/Edit for RUG-II

  Select Supervisor ADT Menu <TEST ACCOUNT> Option: <strong>Recalculate</strong>  G&L Cumulative Totals

  Earliest Date for G&L.....................................MAY 15,2018
  Earliest Date for Treating Specialty Report...............MAY 15,2018
  Earliest Date to Recalculate..............................MAY 15,2018
  SSN Format................................................LAST FOUR OF SSN
  Means Test Copay Applicability............................NOT DISPLAYED
  Patient's Actual Treating Specialty.......................NOT DISPLAYED
  Show Non-Movements on G&L.................................DON'T SHOW
  Store Vietnam Vet's Remaining in CENSUS file..............NO
  Store Patient's over 65 y/o Remaining in CENSUS file......NO

  RECALCULATE TOTALS FROM WHICH DATE: <strong>T-1</strong>   (MAY 15, 2018)
  Requested Start Time: NOW// <strong>&lt;enter&gt;</strong> (MAY 16, 2018@16:10:14)

  Request Queued!</code></div>

Now, let's check that everything is in working order. We will print ``Gains and Losses (G&L) Sheet`` from the
``ADT Outputs Menu``:

.. raw:: html

  <div class="code"><code>Select Supervisor ADT Menu <TEST ACCOUNT> Option:


            ADT Outputs Menu ...
            Bed Control Menu ...
            Beneficiary Travel Menu ...
            Contract Nursing Home RUG Menu ...
            Eligibility Inquiry for Patient Billing
            MAS Code Sheet Manager Menu ...
            Meaningful Use Language Statistics
            Patient Inquiry
            PTF Menu ...
            Registration Menu ...
            RUG-II Menu ...
            Supervisor ADT Menu ...

  Select ADT Manager Menu <TEST ACCOUNT> Option: <strong>ADT</strong> Outputs Menu


            10-10 Print
            ADT Third Party Output Menu ...
            AMIS Reports Menu ...
            Bed Availability
            Disposition Outputs Menu ...
            Enrollment Reports ...
            Gains and Losses (G&L) Sheet
            Inconsistent Data Elements Report
            Inpatient/Lodger Report Menu ...
            Means Test Outputs ...
            N/T Radium Treatment Pending Verification List
            Pending/Open Disposition List
            Print Patient Label
            Scheduled Admission Statistics
            Scheduled Admissions List
            Treating Specialty Print
            VBC Form By Admission Date
            VBC Form for Specific Patient
            Waiting List Output

  Select ADT Outputs Menu <TEST ACCOUNT> Option: <strong>Gains</strong> and Losses (G&L) Sheet

  <<<GAINS & LOSSES SHEET/BED STATUS REPORT/TREATING SPECIALTY REPORT>>>


  Earliest Date for G&L.....................................MAY 15,2018
  Earliest Date for Treating Specialty Report...............MAY 15,2018
  Earliest Date to Recalculate..............................MAY 15,2018
  SSN Format................................................LAST FOUR OF SSN
  Means Test Copay Applicability............................NOT DISPLAYED
  Patient's Actual Treating Specialty.......................NOT DISPLAYED
  Show Non-Movements on G&L.................................DON'T SHOW
  Store Vietnam Vet's Remaining in CENSUS file..............NO
  Store Patient's over 65 y/o Remaining in CENSUS file......NO

  PRINT GAINS AND LOSSES SHEET? Yes// <strong>&lt;enter&gt;</strong>  (Yes)

  PRINT BED STATUS REPORT? Yes//  <strong>&lt;enter&gt;</strong> (Yes)

  PRINT TREATING SPECIALTY REPORT? Yes//  <strong>&lt;enter&gt;</strong> (Yes)

  LAST BED STATUS REPORT TOTALS EXIST FOR MAY 15,2018

  LAST TREATING SPECIALTY REPORT TOTALS EXIST FOR MAY 15,2018

  PRINT REPORTS FOR WHICH DATE: MAY 16,2018//  <strong>&lt;enter&gt;</strong> (MAY 16, 2018)

  SITE: MAIN CAMPUS WHAT WAS THE CENSUS ON MAY 16, 2018? <strong>0</strong>
  CUM PLANNED ADC: <strong>0</strong>
  MONTHLY PLANNED ADC: <strong>0</strong>
  CORRECTIONS TO PREVIOUS G&L'S:
    Edit? NO//<strong>&lt;enter&gt;</strong>

  Note: This output should be printed at a column width of 132.

  DEVICE: HOME// <strong>PNG</strong>

   1 PNG LANDSCAPE   /tmp/
   2 PNG PORTRAIT   /tmp/
  Choose 1-2> <strong>1</strong>  PNG LANDSCAPE  /tmp/

  Do you want your output QUEUED? No// <strong>&lt;enter&gt;</strong>  (No)</code></div>

The output looks as follows. I took the liberty of using GhostPCL to convert all the VistA
output into PNG images to display on this webpage. The first page is the G&L report, which
is empty; 2nd and 3rd are the Bed Status Report, abbreviated as BSR. The 4th page is the 
Treating Specialty Report, or TSR.

.. figure::
   images/WardSetup/gnl01.png
   :align: left
   :alt: G&L page 1
   
   G & L Page 1

.. figure::
   images/WardSetup/gnl02.png
   :align: left
   :alt: G&L page 2
   
   G & L Page 2

.. figure::
   images/WardSetup/gnl03.png
   :align: left
   :alt: G&L page 3

   G & L Page 3

.. figure::
   images/WardSetup/gnl05.png
   :align: left
   :alt: G&L page 4

   G & L Page 4

Extra Credit: Set-up Bulletins
------------------------------
Not covered here, but there is an optional step for you to work on: If you want VistA emails
when an event happens, you can set-up mail groups, add yourself to the mail groups, and then
attach the mail groups to the bulletins.

Here's a list of bulletins that you can receive::

  Select ADT System Definition Menu <TEST ACCOUNT> Option: Bulletin Selection
  This option is used to specify the mailgroup you desire specific types of
  notification to be made to.  The mailgroup can be one created locally or a
  distributed 'DG' mailgroup.  If a mailgroup is selected notification concerning
  that specific action will be made in the form of a mailman bulletin.  If no
  notification is desired for a specific action no mailgroup should be specified.
  If you have any questions concerning the purpose of a specific type of
  notification enter a question mark at the applicable prompt.

  DEATH GROUP:
  NEW PATIENT GROUP:
  NAME CHANGE GROUP:
  SSN CHANGE GROUP:
  UNVERIFIED ADMIT GROUP:
  INCONSISTENCY EDIT GROUP:
  NON-VETERAN ADMIT GROUP:
  OVERDUE ABSENCES GROUP:
  PATIENT DELETED GROUP:
  SENSITIVE REC ACCESSED GROUP:
  SENSITIVITY REMOVED GROUP:
  AUTO RECALC GROUP:
  MEANS TEST REQUIRED GROUP:
  IRT SHORT FORM LIST GROUP:

Setup Gains and Losses Task in Taskman
--------------------------------------
The last step is to make sure that the daily statistics for G&L are recalcuated each
night for the previous day's admission. The task that needs to be scheduled is called
``DG G&L RECALCULATION AUTO``. You need to press enter several times until you are
back up to the System Manager Menu. From there, choose ``Taskman Management`` and then
``Schedule/Unschedule Options``.

.. raw:: html

  <pre>Select Systems Manager Menu <TEST ACCOUNT> Option: <strong>Taskman Management</strong>


            Schedule/Unschedule Options
            One-time Option Queue
            Taskman Management Utilities ...
            List Tasks
            Dequeue Tasks
            Requeue Tasks
            Delete Tasks
            Print Options that are Scheduled to run
            Cleanup Task List
            Print Options Recommended for Queueing

  Select Taskman Management <TEST ACCOUNT> Option: <strong>Sched</strong>ule/Unschedule Options

  Select OPTION to schedule or reschedule: <strong>DG G&L RECALCULATION AUTO</strong>       Auto-re
  calculation of G&L Statistics
    Are you adding 'DG G&L RECALCULATION AUTO' as 
      a new OPTION SCHEDULING (the 13TH)? No// <strong>Y</strong></pre>
  
You will a Screenman screen, like the one we used when we added a new user. Fill in the field
``QUEUED TO RUN AT WHAT TIME`` to ``T+1@0001`` and ``RESCHEDULING FREQUENCY``. The ``TASK ID``
number will be empty until you go to bottom and type "S" (or F1-S, or click on "Save") to
save the entry. You can then Exit ("E", F1-E, or click on Exit) to exit back to the menu system.

.. raw:: html

 <pre>                      Edit Option Schedule
      Option Name: DG G&L RECALCULATION AUTO
      Menu Text: Auto-recalculation of G&L Statis          TASK ID: 1115
    __________________________________________________________________________

    QUEUED TO RUN AT WHAT TIME: <strong>T+1@0001</strong>

  DEVICE FOR QUEUED JOB OUTPUT:

   QUEUED TO RUN ON VOLUME SET:

        RESCHEDULING FREQUENCY: <strong>1D</strong>

               TASK PARAMETERS:

              SPECIAL QUEUEING:

  _______________________________________________________________________________

  Exit    Save    Next Page    Refresh    Quit

  Click on one of the above COMMANDs, or on a FIELD

  COMMAND: E                                                        HELP  Insert</pre>


Continue on to `Admit Patients <./AdmitPatients.html>`_
