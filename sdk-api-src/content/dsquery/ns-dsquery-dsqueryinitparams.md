---
UID: NS:dsquery.__unnamed_struct_0
title: DSQUERYINITPARAMS
author: windows-sdk-content
description: Describes the data used to initialize a browse dialog box in the directory service query.
old-location: ad\dsqueryinitparams.htm
tech.root: ad
ms.assetid: ff1cb792-efb0-46f5-bc9b-95c9fb2959db
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPDSQUERYINITPARAMS, DSQPF_ENABLEADMINFEATURES, DSQPF_ENABLEADVANCEDFEATURES, DSQPF_HASCREDENTIALS, DSQPF_NOCHOOSECOLUMNS, DSQPF_NOSAVE, DSQPF_SAVELOCATION, DSQPF_SHOWHIDDENOBJECTS, DSQUERYINITPARAMS, DSQUERYINITPARAMS structure [Active Directory], LPDSQUERYINITPARAMS, LPDSQUERYINITPARAMS structure pointer [Active Directory], _glines_dsqueryinitparams, ad.dsqueryinitparams, dsquery/DSQUERYINITPARAMS, dsquery/LPDSQUERYINITPARAMS"
ms.topic: struct
req.header: dsquery.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dsquery.h
api_name:
 - DSQUERYINITPARAMS
product: Windows
targetos: Windows
req.typenames: DSQUERYINITPARAMS, *LPDSQUERYINITPARAMS
req.redist: 
---

# DSQUERYINITPARAMS structure


## -description


The <b>DSQUERYINITPARAMS</b> structure describes the data used to initialize a browse dialog box in the directory service query.


## -struct-fields




### -field cbStruct

Contains the size, in bytes,  of this structure.


### -field dwFlags

Contains a set of flags that define the query behavior. This can be zero or a combination of one or more of the following values.



#### DSQPF_ENABLEADMINFEATURES

Uses features supported by the directory service administration tools, such as Admin Display Specifier for context menus and property pages.



#### DSQPF_ENABLEADVANCEDFEATURES

Specifies advanced features in the <a href="https://msdn.microsoft.com/en-us/library/ms688421(v=VS.85).aspx">IDataObject</a> instance passed to context menus and property pages.



#### DSQPF_HASCREDENTIALS

The <b>pUserName</b>, <b>pPassword</b> and <b>pServer</b> members of this structure can specify server and credential data.



#### DSQPF_NOCHOOSECOLUMNS

Disables the <b>Choose Columns</b> item in the query dialog box <b>View</b> menu.



#### DSQPF_NOSAVE

Removes the <b>Save Search</b> item from the query dialog box <b>File</b> menu.



#### DSQPF_SAVELOCATION

The <b>pDefaultSaveLocation</b> member contains the default file system path where searches will be saved.



#### DSQPF_SHOWHIDDENOBJECTS

Causes the query dialog box to display hidden objects in the query results list.


### -field pDefaultScope

Pointer to a null-terminated Unicode string that contains the ADsPath of the default scope for the search. Set this member to <b>NULL</b> if no default search scope is specified.


### -field pDefaultSaveLocation

Pointer to a null-terminated Unicode string that contains the default file system path where searches will be saved. This member is ignored if the <b>dwFlags</b> member does not contain <b>DSQPF_SAVELOCATION</b>.


### -field pUserName

Pointer to a  null-terminated Unicode string that contains the user name in the valid domain notation, for example, "fabrikam\jeffsmith".


### -field pPassword

Pointer to a  null-terminated Unicode string that contains the password of the user specified by the <b>pUserName</b> member.


### -field pServer

Pointer to  a  null-terminated Unicode string that contains the name of the server from which the list of trusted domains is read. The list is used to populate the <b>In:</b> drop-down list in the dialog box.


## -remarks



This structure is specific to the <b>CLSID_DsQuery</b> query handler. This structure is used for the <b>pHandlerParameters</b> member of the <a href="https://msdn.microsoft.com/07ef2af1-230e-41d9-ad19-d002d0579d66">OPENQUERYWINDOW</a> structure when <b>CLSID_DsQuery</b> is set for the <b>clsidHandler</b> member of the 
<b>OPENQUERYWINDOW</b> structure. For more information, and a code example for  using this, and other related APIs, see 
<a href="https://msdn.microsoft.com/604c4d7a-1f85-4e5b-9879-be502c5c7bff">ICommonQuery::OpenQueryWindow</a>.




## -see-also




<a href="https://msdn.microsoft.com/bf6aa066-ee7e-4b13-9a4b-1e097632ec5a">Active
  Directory Display Structures</a>



<a href="https://msdn.microsoft.com/604c4d7a-1f85-4e5b-9879-be502c5c7bff">ICommonQuery::OpenQueryWindow</a>



<a href="https://msdn.microsoft.com/en-us/library/ms688421(v=VS.85).aspx">IDataObject</a>



<a href="https://msdn.microsoft.com/07ef2af1-230e-41d9-ad19-d002d0579d66">OPENQUERYWINDOW</a>
 

 

