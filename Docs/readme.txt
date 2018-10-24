Paper:
Bayesian Multi-faceted models for measuring classroom professor's performance, and subject's relevance

Authors
Alvaro Montenegro, Harvey Rosas, Campo El\'ias Pardo, Eduardo Jorquera, Cristian Mill\'an, Jhonatan Medina



Abstract
This file contains the description of the data and codes of the paper.

Docs.
=================================================
Questionary UN Professor.xls
=================================================
Original complete questionary. Spanish

R-codes.
=================================================
R1_Multi_Faceted_Ciencias_Data_Preparation.
=================================================
1. Read the file D2_Sample_Data_To_Stan.txt 
2. Compute the response categories.
3. Professor's performance. Fix the categories 1,2, as categoriy 1 to have 4 categories
4. Subject's relevance. Fix the categories 1,2, as category 1 to have 4 categories
5. Create the plot unidimensional_analysis.png from professor items
6. feate the files
D3_Sample_Data_recode.txt, with recode categories (4 cateories for professor and subject data), Id students, 
   profesors, and subjects. Include the original Id key of the table for returning to original data
D4_professor_data_sample.txt. Professor data, ready to Stan
D5_subject_data_sample.txtready . Subject data, ready to Stan



Stan-codes
S1_

Data files
=================================================
D1_Complete_Data_Base_Faculty.txt
=================================================
This file contains the complete data

There are 14703 registers,  and 39 columns. Columns are separated by semicolon (;). First row contains the name of the columns.

student data: columns 1 to 6 ("Id_Student";"tbl_Student_sex";"Carrer";"Number_Enrollment";"Number_Repetition";"Self_Perfomance";). 

subject data: columns 7,8,9,10,11 ("Group"; "Id_Course";"Id_Carrer";"Id_Subject";"Shared";)

professor data: columns 12,13,14 ("Id_Professor";"tbl_Professor_sex";"Department";)

categorical survey responses: columns 15 to 37 ("C_12";"C_13";"C_14";"C_15";"C_16";"C_17";"C_18";"C_19";"C_20";"C_21";"C_22";"C_23";"C_24";"C_25";
"C_26";"C_27";"C_28";"C_29";"C_30";"C_31";"C_32";"C_33";"C_34";"C_35";)

textual survey responses: columns 38 to 39 ("C_36_Strength";"c37_Weaknesses")

#The professor's performance responses are C_12 to C_17, C_21:C_28 and C_34
#The subject's relevance responses are C_18:C20, and C35
# Physical resources responses (not used) C_29 to C_33

=================================================
D2_Sample_Data.txt
=================================================
This file contains the data selected to the experiments
# We use this sample for experiments
# 1380  registers, corresponding to 123 subjects, with 4 to 20 registers, 
# 36 carrers with 3 to 223 registers, 124 professors wit 3 to 36 registers. 


# Data description
# student data
# datos[,1]: Id_Student. This is the key of the table
# datos[,2]: student sex
# datos[,3]: Id_Fingerprint. Groups of simmilar characteristics
# datos[,4]: Id_Carrer. Id of the student carrer
# datos[,5]: Number_Enrollment
# datos[,6]: Number_Repetition
# datos[,7]: Number_Lost
# datos[,8]: Self_Perfomance
# subject data
# datos[,9]: Id_Subject
# datos[,10]: Id_Course
# datos[,11]: Group
# datos[,12]: Shared. 1= shared course; 0 = no shared course
# professor data
# datos[,13]: Id_professor. Id of the professor of the course
# datos[,14]: professor_sex. Id of the professor of the course
# datos[,15]: Vinculacion prof: Planta, ocasional
# datos[,16]: Fecha_Ingreso UN
# datos[,17]: professor_cat: category of professor
# datos[,18]: professor_dedic: dedication of the prof.
# datos[,19]: professor_Dept: Departament of the prof.
# item responses
# datos[,20:43]: items: C_12 to C_35; professor: C_12:C_17; C_22:C_28; C_34;
#                                       subject: C_18:C_21; C_35
#                            Physical resources: C_29:C31
#                                       Monitor: C_32:C_33
# textual responses 
# datos[,44:45]: questions C_36 (Strength) and C_37 (Weaknesses)
#
##################################################################
#
=================================================
D3_Sample_Data_recode.txt
=================================================
This file contains the same data as fikle D2_Sample_Data.txt,
exept that the categories of response items are recode to 1,2,3, and 4.

