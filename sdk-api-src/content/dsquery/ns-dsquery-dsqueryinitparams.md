---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

Specifies advanced features in the <a href="_ole_idataobject">IDataObject</a> instance passed to context menus and property pages.



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



<a href="_ole_idataobject">IDataObject</a>



<a href="https://msdn.microsoft.com/07ef2af1-230e-41d9-ad19-d002d0579d66">OPENQUERYWINDOW</a>
 

 

