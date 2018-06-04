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

# IGPMMigrationTable::AddEntry


## -description


Creates an entry in the migration table. The method  updates an existing entry.


## -parameters




### -param bstrSource [in]

Source field of the entry. This parameter cannot be null.


### -param gpmEntryType [in]

This parameter must be one of the following values.



#### typeUser

This value  equals 0 (zero). Creates a User entry in the migration table.



#### typeComputer

Creates a  entry for a User.



#### typeLocalGroup

Creates an entry  for a LocalGroup.



#### typeGlobalGroup

Creates an entry for a GlobalGroup.



#### typeUniversalGroup

Creates an entry for a UniversalGroup.



#### typeUNCPath

Creates an entry for a UNCPath.



#### typeUnknown

Creates an entry for an unknown.


### -param pvarDestination [in, optional]

A pointer to a <b>VARIANT</b> structure.  You can  use the <b>DestinationOptions</b>: <b>opDestinationSameAsSource</b>, <b>opDestinationNone</b>, or <b>opDestinationByRelativeName</b> by passing  in a <i>pvarDestination</i> with a <b>vt</b> member of VT_I4. To explicitly pass in the destination,  pass in a <i>pvarDestination</i> with a <b>vt</b> member of VT_BSTR, and this  sets the <b>DestinationOptions</b> to <b>opDestinationSet</b>. If you pass in null, <b>AddEntry</b> uses the default value for the destination option, <b>opDestinationSameAsSource</b>.


### -param ppEntry [out]

The new entry.


#### - destination [in, optional]

This parameter specifies the destination  as a string or as a destination option. Passing a string for the destination implicitly sets the entry's <a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">DestinationOptionSet</a> equal to the <b>DestinationOptionSet</b> property of the <a href="https://msdn.microsoft.com/e9137167-4a2d-4cc4-940e-20f9991c4187">GPMConstants</a> object.  The destination can also be specified by passing the <b>DestinationSameAsSource</b>, <b>DestinationNone</b>, or <b>DestinationByRelativeName</b> properties of the <b>GPMConstants</b> object.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMMapEntry</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMMapEntry</b> object.




## -see-also




<a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">IGPMMigrationTable</a>
 

 

