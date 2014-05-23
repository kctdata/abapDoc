abapDoc
=======

ABAPdoc: Generate technical documentation

Repository and DDIC object that are contained in this transport are prefixed with Z*KCT_ABAP_DOC* (it is not a SAP namespace) to avoid collision with existing customer specific development.

ABAPdoc is based on components SAP_BASIS and SAP_ABA 7.00 (SAP ECC 6.00) with no dependence on other than standard SAP objects.

User manual is contained directly in the header of the main report ZKCT_ABAP_DOC and also in its SAP documentation.

KCT ABAPdoc can be easily extended by plug-ins for other types of objects; or current plug-ins can be modified to fulfill needs of the user. 

(Plug-in is a class derived from ZCL_KCT_ABAP_DOC; method RENDER_ADD_INFO then generates DOCX output.)

We will be glad if you send plug-ins developed by you to us (ideally as a SAPlink nugget). After the revision of these plugins we will publish them on Github for other users.

If you need ABAPdoc in a form of SAPlink nuggets, contact us on  abapdoc@kctdata and we will export it for you.
 
List of included Plug-ins (supported Object types):
BSP
CLASS
DOMAIN
DATA ELEMENT
FUNCTION GROUP (+FUNCTION MODULE)
NUMBER RANGE
PROGRAM
SEARCH HELP
(DDIC) TABLE
TABLE TYPE
WDC (Web Dynpro)
 



*&---------------------------------------------------------------------*
*& Program         ZKCT_ABAP_DOC
*&
*&---------------------------------------------------------------------*
*& This report is the main part of a Documentation tool developed by
*& KCT Data company (hereinafter KCT ABAPdoc),
*& intended to generate technical documentation of customer's
*& ABAP development.
*&
*&---------------PURPOSE-----------------------------------------------*
*& The purpose of this tool is to generate a technical documentation
*& which, when added to a Functional specification document, significantly
*& helps to complete a complex documentation of your solution.
*& It can also help to generate "JavaDoc like", API documentation
*& of your reusable SW components (FMs, class methods, ..)
*& and last but not least - it can help you to check your developers
*& compliance to required coding conventions and also motivate them
*& to use standard ABAP workbench documentation means (used as a
*& KCT ABAPdoc sources) for consistent and rich documentation
*& of the development.
*&
*&---------------HOW IT WORKS------------------------------------------*
*& It generates a MS Word document (DOCX format) with a list of all
*& the common repository object types including their attributes,
*& descriptions, comments in the source-code (started e.g. with " *& ")
*& and program  documentation (see SELECT-OPTIONS so_krep and
*& application-specific others).
*& Its technical design is inspired by the SAPlink tool (easily
*& enhanceable, having plug-in class for each object type etc.) which
*& has a similar user interface as well.
*&
*&---------------WARRANTIES--------------------------------------------*
*& KCT ABAPdoc is distributed in the hope that it will be useful, but
*& WITHOUT ANY WARRANTY; without even the implied warranty of
*& MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU
*& General Public License for more details.
*&
*&---------------LICENSING---------------------------------------------*
*& KCT ABAPdoc is a free software, you can redistribute it and/or modify
*& it under the terms of the GNU General Public License as published by
*& the Free Software Foundation; either version 3 of the License, or (at
*& your option) any later version,  when done under the brand
*& PERFORMED BY KCT DATA.
*&
*& No renaming of the tool or hiding the brand or author is allowed.
*&
*& You should have received a copy of the GNU General Public License
*& along with this program. If not, see <http://www.gnu.org/licenses/>.
*&
*& Copyright (C)
