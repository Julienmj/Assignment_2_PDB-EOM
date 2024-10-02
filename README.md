# Assignment_2_PDB-EOM
pluggable database creation and oracle entreprise manager creation



#Create Pluggable Database (ju_plsqlauca):

>CREATE PLUGGABLE DATABASE ju_plsqlauca
  ADMIN USER pdb_admin IDENTIFIED BY aucastudent
  ROLES = (DBA)
  DEFAULT TABLESPACE users
  DATAFILE 'C:\Oracle\PDBs\ju_plsqlauca_users01.dbf' SIZE 250M AUTOEXTEND ON
  FILE_NAME_CONVERT = ('C:\ORACLE19C\ORADATA\ORCL\PDBSEED\', 'C:\Oracle\PDBs\ju_plsqlauca\')
  TEMPFILE REUSE;

#Create Another Pluggable Database (ju_to_delete_pdb):

>CREATE PLUGGABLE DATABASE ju_to_delete_pdb
  ADMIN USER pdb_admin IDENTIFIED BY aucastudent
  ROLES = (DBA)
  DEFAULT TABLESPACE users
  DATAFILE 'C:\Oracle\PDBs\ju_to_delete_pdb_users01.dbf' SIZE 250M AUTOEXTEND ON
  FILE_NAME_CONVERT = ('C:\ORACLE19C\ORADATA\ORCL\PDBSEED\', 'C:\Oracle\PDBs\ju_to_delete_pdb\')
  TEMPFILE REUSE;


#Drop Pluggable Database (ju_to_delete_pdb):

>DROP PLUGGABLE DATABASE ju_to_delete_pdb INCLUDING DATAFILES;

![Screenshot (35)](https://github.com/user-attachments/assets/00fe92c6-e3d7-4b1e-bc59-a0d823031835)

# Oracle Enterprise Manager:
1.Opening the Pluggable Database:

>ALTER PLUGGABLE DATABASE JU_PLSQLAUCA OPEN;


2.connecting eom in cmd:

>C:\Users\julie>sqlplus sys/Kibra2004@localhost:1521/ORCL as sysdba

#EOM dashboard

![Screenshot (36)](https://github.com/user-attachments/assets/f4834cab-d983-432f-b48d-975e303f339a)

![Screenshot (37)](https://github.com/user-attachments/assets/63bc1c5b-16a5-42cb-9505-8f31effb08d8)

![Screenshot (39)](https://github.com/user-attachments/assets/aa9c621c-910d-4a6d-bf0c-b17b8beaf5cc)



