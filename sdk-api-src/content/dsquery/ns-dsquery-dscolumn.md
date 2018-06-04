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

# DSCOLUMN structure


## -description


The <b>DSCOLUMN</b> structure represents a column in the directory services query dialog box. An array of this structure is contained in the <a href="https://msdn.microsoft.com/78c3fb1c-275e-45b6-bbe9-ae2d85864e6a">DSQUERYPARAMS</a> structure.


## -struct-fields




### -field dwFlags

Reserved.


### -field fmt

Contains one of the list view column formatting values that indicates how the column is displayed. The possible values are defined for the <b>fmt</b> member of the <a href="_win32_lvcolumn_cpp">LVCOLUMN</a> structure.


### -field cx

Contains the width, in pixels, of the column.


### -field idsName

Contains the string table identifier for the column header string. To retrieve this string, call  <a href="_win32_loadstring_cpp">LoadString</a> with the <b>hInstance</b> member of the <a href="https://msdn.microsoft.com/78c3fb1c-275e-45b6-bbe9-ae2d85864e6a">DSQUERYPARAMS</a> structure and this member for the string identifier.


### -field offsetProperty

Indicates the name of the attribute displayed in the column. This can be one of the following values.



#### DSCOLUMNPROP_ADSPATH

The column displays the value of the ADsPath of the object.



#### DSCOLUMNPROP_OBJECTCLASS

The column displays the value of the <b>objectClass</b> of the object.

If this member does not contain one of these values, this member contains the offset, in bytes, from the address of the <a href="https://msdn.microsoft.com/78c3fb1c-275e-45b6-bbe9-ae2d85864e6a">DSQUERYPARAMS</a> structure to a null-terminated  Unicode string that contains the name of the  attribute value displayed in this column.


### -field dwReserved

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/78c3fb1c-275e-45b6-bbe9-ae2d85864e6a">DSQUERYPARAMS</a>



<a href="https://msdn.microsoft.com/bf6aa066-ee7e-4b13-9a4b-1e097632ec5a">Display Structures in Active Directory Domain Services</a>



<a href="https://msdn.microsoft.com/604c4d7a-1f85-4e5b-9879-be502c5c7bff">ICommonQuery::OpenQueryWindow</a>



<a href="_win32_lvcolumn_cpp">LVCOLUMN</a>



<a href="_win32_loadstring_cpp">LoadString</a>
 

 

