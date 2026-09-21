# Oracle PDB Assignment II

## Overview
This project demonstrates creating a pluggable database (PDB) with a dedicated
user, creating and deleting a temporary PDB, and configuring Oracle Enterprise
Manager (OEM) to monitor the environment.

## Oracle Environment
Oracle Database 21c Enterprise Edition (21.3.0.0.0), running locally on
Windows, CDB name: ORCL.

## Task Explanations

### Task 1: Create a New Pluggable Database
Created PDB `og_pdb_28518` from the seed database, opened it, and created a
dedicated user `oganze_plsqlauca_28518` inside it with CONNECT, RESOURCE, and
DBA privileges. A USERS tablespace was manually created inside the PDB since
it was not present by default after cloning from the seed.

### Task 2: Create and Delete a PDB
Created a temporary PDB `og_to_delete_pdb_28518`, verified it existed and was
open, then closed it and dropped it including its datafiles. Verified deletion
by confirming it no longer appears in `v$pdbs`.

### Task 3: OEM Setup
Accessed Oracle Enterprise Manager Database Express at
https://localhost:5500/em, confirmed the dashboard reflects the ORCL CDB and
its PDBs (including og_pdb_28518), and captured a screenshot with the sys
username visible.

## Challenges Faced
The USERS tablespace did not exist by default in the newly created PDB,
causing the initial CREATE USER command to fail with ORA-00959. This was
resolved by manually creating the USERS tablespace before creating the user.

## Integrity Statement
I confirm this work is my own and was completed according to the assignment
guidelines.

## Submission Details
Repository Link: https://github.com/venusse40/oracle_pdb_ass_II_28518_oganze
PDB Name Created: og_pdb_28518
Issues Encountered: Yes