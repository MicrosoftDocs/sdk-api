---
UID: NS:cmnquery.OPENQUERYWINDOW
title: OPENQUERYWINDOW (cmnquery.h)
description: Used with the ICommonQuery::OpenQueryWindow method to initialize the directory service query dialog box.
helpviewer_keywords: ["*LPOPENQUERYWINDOW","CLSID_DsFindAdvanced","CLSID_DsFindComputer","CLSID_DsFindContainer","CLSID_DsFindDomainController","CLSID_DsFindFrsMembers","CLSID_DsFindObjects","CLSID_DsFindPeople","CLSID_DsFindPrinter","CLSID_DsFindVolume","CLSID_DsFindWriteableDomainController","CLSID_DsQuery","LPOPENQUERYWINDOW","LPOPENQUERYWINDOW structure pointer [Active Directory]","OPENQUERYWINDOW","OPENQUERYWINDOW structure [Active Directory]","OQWF_DEFAULTFORM","OQWF_HIDEMENUS","OQWF_HIDESEARCHUI","OQWF_ISSUEONOPEN","OQWF_LOADQUERY","OQWF_OKCANCEL","OQWF_PARAMISPROPERTYBAG","OQWF_REMOVEFORMS","OQWF_REMOVESCOPES","OQWF_SAVEQUERYONOK","OQWF_SHOWOPTIONAL","OQWF_SINGLESELECT","_glines_openquerywindow","ad.openquerywindow","cmnquery/LPOPENQUERYWINDOW","cmnquery/OPENQUERYWINDOW"]
old-location: ad\openquerywindow.htm
tech.root: ad
ms.assetid: 07ef2af1-230e-41d9-ad19-d002d0579d66
ms.date: 12/05/2018
ms.keywords: '*LPOPENQUERYWINDOW, CLSID_DsFindAdvanced, CLSID_DsFindComputer, CLSID_DsFindContainer, CLSID_DsFindDomainController, CLSID_DsFindFrsMembers, CLSID_DsFindObjects, CLSID_DsFindPeople, CLSID_DsFindPrinter, CLSID_DsFindVolume, CLSID_DsFindWriteableDomainController, CLSID_DsQuery, LPOPENQUERYWINDOW, LPOPENQUERYWINDOW structure pointer [Active Directory], OPENQUERYWINDOW, OPENQUERYWINDOW structure [Active Directory], OQWF_DEFAULTFORM, OQWF_HIDEMENUS, OQWF_HIDESEARCHUI, OQWF_ISSUEONOPEN, OQWF_LOADQUERY, OQWF_OKCANCEL, OQWF_PARAMISPROPERTYBAG, OQWF_REMOVEFORMS, OQWF_REMOVESCOPES, OQWF_SAVEQUERYONOK, OQWF_SHOWOPTIONAL, OQWF_SINGLESELECT, _glines_openquerywindow, ad.openquerywindow, cmnquery/LPOPENQUERYWINDOW, cmnquery/OPENQUERYWINDOW'
req.header: cmnquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OPENQUERYWINDOW, *LPOPENQUERYWINDOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPOPENQUERYWINDOW
 - cmnquery/LPOPENQUERYWINDOW
 - OPENQUERYWINDOW
 - cmnquery/OPENQUERYWINDOW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Cmnquery.h
api_name:
 - OPENQUERYWINDOW
---

# OPENQUERYWINDOW structure


## -description

The <b>OPENQUERYWINDOW</b> structure is used with 
   the <a href="/windows/desktop/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow">ICommonQuery::OpenQueryWindow</a> method to 
   initialize the directory service query dialog box.

## -struct-fields

### -field cbStruct

Contains the size, in bytes, of the structure. This member is used for versioning and parameter validation 
      and must be filled in before calling 
      <a href="/windows/desktop/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow">ICommonQuery::OpenQueryWindow</a>.

### -field dwFlags

Contains a set of flags that define the behavior of the directory service query dialog box. This can be 
      zero or a combination of one or more of the values listed in the following list.



#### OQWF_DEFAULTFORM

Causes the query dialog box to select the form specified by the 
        <b>clsidDefaultForm</b> member on initialization.



#### OQWF_HIDEMENUS

Causes the  dialog box to hide the menu bar.



#### OQWF_HIDESEARCHUI

Causes the query dialog box to be  created without the standard  search user interface. This includes the 
        <b>Find Now</b>, <b>Stop</b> and 
        <b>Clear All</b> pushbuttons.



#### OQWF_ISSUEONOPEN

Causes the query to be executed when the query dialog box is first displayed.



#### OQWF_LOADQUERY

Causes the query dialog box to retrieve the query from the 
        <a href="/windows/desktop/api/cmnquery/nn-cmnquery-ipersistquery">IPersistQuery</a> interface in the 
        <b>pPersistQuery</b> member.



#### OQWF_OKCANCEL

Causes the query dialog box to display the <b>OK</b> and 
        <b>Cancel</b> buttons, if applicable. The buttons actually displayed in the dialog box 
        will depend on the form used and other specified flags.



#### OQWF_PARAMISPROPERTYBAG

Indicates that the <b>ppbFormParameters</b> member contains an 
        <a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a> interface.



#### OQWF_REMOVEFORMS

Causes the query dialog box to be created without the form chooser label and drop-down list represented 
        by the <b>Find:</b> label.



#### OQWF_REMOVESCOPES

Causes the query dialog box to be created without the scope label and drop-down list represented by the 
        <b>In:</b> label.



#### OQWF_SAVEQUERYONOK

Causes the query dialog box, when closed, to save the query to the 
        <a href="/windows/desktop/api/cmnquery/nn-cmnquery-ipersistquery">IPersistQuery</a> interface in the 
        <b>pPersistQuery</b> member.



#### OQWF_SHOWOPTIONAL

Causes the query dialog box to display optional forms in the form drop-down list. Optional forms are 
        forms that specify the <b>CQFF_ISOPTIONAL</b> flag in the 
        <b>dwFlags</b> member of the <a href="/windows/desktop/api/cmnquery/ns-cmnquery-cqform">CQFORM</a> 
        structure.



#### OQWF_SINGLESELECT

Causes the query dialog box to make the query results list single-selection.

### -field clsidHandler

Contains a <b>CLSID</b> value that specifies the query handler to be used by the 
      query dialog box. The value of this member also determines the type of structure pointed to by the 
      <b>pHandlerParameters</b> member.



#### CLSID_DsQuery

This is the standard directory service query and the only currently supported query.

### -field pHandlerParameters

Pointer to a structure that contains data for the query handler. The type of structure pointed to by this 
      member is defined by the <b>clsidHandler</b> member. The following list lists the possible 
      types of structures based on the value of the <b>clsidHandler</b> member.



#### CLSID_DsQuery

Contains a pointer to a <a href="/windows/desktop/api/dsquery/ns-dsquery-dsqueryinitparams">DSQUERYINITPARAMS</a> 
        structure.

### -field clsidDefaultForm

Specifies the default form to be displayed in the query dialog box. This member is ignored if 
      <b>dwFlags</b> does not contain <b>OQWF_DEFAULTFORM</b>. This member can 
      contain the <b>CLSID</b> of a custom query form or one of the system-supplied forms.



#### CLSID_DsFindAdvanced

Identifies the <b>Custom Search</b> query form.



#### CLSID_DsFindComputer

Identifies the <b>Computers</b> query form.



#### CLSID_DsFindContainer

Identifies the <b>Organizational Units</b> query form.



#### CLSID_DsFindDomainController

Identifies the <b>Domain Controllers</b> query form.



#### CLSID_DsFindFrsMembers

Identifies the <b>FRS Members</b> query form.



#### CLSID_DsFindObjects

Reserved.



#### CLSID_DsFindPeople

Identifies the <b>Users, Contacts, and Groups</b> query form.



#### CLSID_DsFindPrinter

Identifies the <b>Printers</b> query form.



#### CLSID_DsFindVolume

Identifies the <b>Shared Folders</b> query form.



#### CLSID_DsFindWriteableDomainController

Identifies the <b>Domain Controllers</b> query form and displays writable Domain 
        Controllers.

### -field pPersistQuery

Pointer to an <a href="/windows/desktop/api/cmnquery/nn-cmnquery-ipersistquery">IPersistQuery</a> interface used 
      to store and retrieve query data. This data pertains to the query itself, not the results of the query. If 
      <b>dwFlags</b> contains <b>OQWF_LOADQUERY</b>, the query data is obtained 
      from this interface. If <b>dwFlags</b> contains <b>OQWF_SAVEQUERY</b>, 
      the query data is saved to this interface.

### -field pFormParameters

Reserved. Pointer to a structure or interface that provides parameter initialization data for the form. 
       The contents of this pointer is defined by the form class specified by the 
       <b>clsidDefaultForm</b> member.

### -field ppbFormParameters

Pointer to an <a href="../oaidl/nn-oaidl-ipropertybag.md">IPropertyBag</a> interface that 
       provides parameter initialization data for the form. The contents of this property bag are defined by the form 
       class specified by the <b>clsidDefaultForm</b> member. The following system-supplied forms 
       support this member.



#### CLSID_DsFindPrinter

This form obtains the following properties from the property bag.

<table>
<tr>
<th>Property name</th>
<th>Description</th>
</tr>
<tr>
<td>
printName

</td>
<td>
Contains the initial printer name.

</td>
</tr>
<tr>
<td>
printLocation

</td>
<td>
Contains the initial printer location.

</td>
</tr>
<tr>
<td>
printModel

</td>
<td>
Contains the initial model name and/or number of the printer.

</td>
</tr>
</table>
 



#### CLSID_DsFindComputer

Use this form to specify the computer roles. The property bag must include computerRole. Use a combination 
          of the following values to restrict which roles are included:

<table>
<tr>
<th>Value</th>
<th>Role</th>
</tr>
<tr>
<td>
0x0000

</td>
<td>
All roles

</td>
</tr>
<tr>
<td>
0x0001

</td>
<td>
Workstation or Server

</td>
</tr>
<tr>
<td>
0x0002

</td>
<td>
All Domain Controllers

</td>
</tr>
<tr>
<td>
0x0004

</td>
<td>
Writable Domain Controllers

</td>
</tr>
<tr>
<td>
0x0008

</td>
<td>
Read-only Domain Controllers

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/cmnquery/ns-cmnquery-cqform">CQFORM</a>



<a href="/windows/desktop/api/dsquery/ns-dsquery-dsqueryinitparams">DSQUERYINITPARAMS</a>



<a href="/windows/desktop/AD/display-structures-in-active-directory-domain-services">Display Structures in Active Directory Domain Services</a>



<a href="/windows/desktop/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow">ICommonQuery::OpenQueryWindow</a>



<a href="/windows/desktop/api/cmnquery/nn-cmnquery-ipersistquery">IPersistQuery</a>

