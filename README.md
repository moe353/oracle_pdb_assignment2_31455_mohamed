# oracle_pdb_assignment2_31455_mohamed
# Assignment II: Oracle Pluggable Database (PDB) Administration

## 1. Assignment Overview
This assignment demonstrates the practical administration of Oracle 21c Multitenant Architecture. It focuses on hands-on deployment, which includes creating, configuring, managing, and deleting Pluggable Databases (PDBs) along with database users inside a PDB environment.

## 2. Oracle Environment
- **Oracle Version:** Oracle Database 21c Express Edition (XE)
- **Operating System:** Windows
- **Tools Used:** SQL*Plus, Oracle Enterprise Manager (OEM) Database Express

## 3. Task Documentation
- **PDB Creation:** Successfully created the pluggable database `mo_pdb_31455` and opened it under the CDB$ROOT container.
- **User Configuration:** Created the local database user `mohamed_plsqlauca_31455` inside the `mo_pdb_31455` container and assigned CONNECT, RESOURCE, and administrative privileges.
- **Temporary PDB Creation and Deletion:** Created a temporary pluggable database named `mo_to_delete_pdb_31455` using precise file paths for Windows. Verified its status, closed it, and dropped it completely including its datafiles.
- **OEM Configuration:** Accessed the Oracle Enterprise Manager dashboard via HTTPS port 5500 to review the structural state of the pluggable database environment.

## 4. Challenges and Solutions
- **Challenge 1:** Encountered `ERROR: ORA-01031: insufficient privileges` when attempting to switch back to the `CDB$ROOT` container.
  - *Solution:* Reconnected immediately to the session using administrative system credentials via `CONNECT / AS SYSDBA`.
- **Challenge 2:** Encountered `ERROR: ORA-65005: missing or invalid file name pattern` during the temporary PDB initialization.
  - *Solution:* Resolved the path collision by mapping explicit Windows absolute directory locations inside the `FILE_NAME_CONVERT` clause.

## 5. Lessons Learned
- Developed a concrete technical understanding of the Oracle Multitenant Architecture.
- Mastered structural SQL*Plus administration operations including data file conversions and localized user permission maps.
- Gained hands-on experience troubleshooting Windows-specific Oracle system errors.

## 6. Integrity Statement
"I confirm that this assignment represents my own practical work, screenshots, and documentation. All external resources consulted have been properly acknowledged."
