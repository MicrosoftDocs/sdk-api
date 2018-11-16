---
UID: NF:gpmgmt.IGPMMigrationTable.AddEntry
title: IGPMMigrationTable::AddEntry
author: windows-sdk-content
description: Creates an entry in the migration table. The method updates an existing entry.
old-location: gpmc\igpmmigrationtable_addentry.htm
tech.root: GPMC
ms.assetid: 2e6f6b81-b01c-4d46-9b7b-3265580f112a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AddEntry, AddEntry method [GPMC], AddEntry method [GPMC],GPMMigrationTable class, AddEntry method [GPMC],IGPMMigrationTable interface, GPMMigrationTable class [GPMC],AddEntry method, IGPMMigrationTable interface [GPMC],AddEntry method, IGPMMigrationTable.AddEntry, IGPMMigrationTable::AddEntry, gpmc.igpmmigrationtable_addentry, gpmgmt/IGPMMigrationTable::AddEntry, typeComputer, typeGlobalGroup, typeLocalGroup, typeUNCPath, typeUniversalGroup, typeUnknown, typeUser
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMMigrationTable.AddEntry
 - GPMMigrationTable.AddEntry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- gpmgmt.h
: 
- IGPMMigrationTable.AddEntry
: 
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
 

 

