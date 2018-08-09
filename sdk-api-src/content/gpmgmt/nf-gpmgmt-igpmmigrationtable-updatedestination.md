---
UID: NF:gpmgmt.IGPMMigrationTable.UpdateDestination
title: IGPMMigrationTable::UpdateDestination
author: windows-sdk-content
description: Updates the destination field of an entry in a migration table. You can specify the destination option and the destination.
old-location: gpmc\igpmmigrationtable_updatedestination.htm
old-project: GPMC
ms.assetid: c47ad9d7-cf04-4ab4-9c44-78a5e54fc04e
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GPMigrationTable class [GPMC],UpdateDestination method, IGPMMigrationTable interface [GPMC],UpdateDestination method, IGPMMigrationTable.UpdateDestination, IGPMMigrationTable::UpdateDestination, UpdateDestination, UpdateDestination method [GPMC], UpdateDestination method [GPMC],GPMigrationTable class, UpdateDestination method [GPMC],IGPMMigrationTable interface, gpmc.igpmmigrationtable_updatedestination, gpmgmt/IGPMMigrationTable::UpdateDestination
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: GPMStarterGPOType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMMigrationTable.UpdateDestination
 - GPMigrationTable.UpdateDestination
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGPMMigrationTable::UpdateDestination


## -description


Updates the destination field of an entry in a migration table. You can specify the destination option and the destination.


## -parameters




### -param bstrSource [in]

The source field of the migration table which is to be updated.


### -param pvarDestination [in, optional]

A pointer to a <b>VARIANT</b> structure.  You can  use the DestinationOptions: opDestinationSameAsSource, opDestinationNone, or opDestinationByRelativeName by passing  in a <i>pvarDestination</i> with a <b>vt</b> member of VT_I4. To explicitly pass in the destination,  pass in a <i>pvarDestination</i> with a <b>vt</b> member of VT_BSTR, and this will set the DestinationOption to opDestinationSet. If you pass in null, UpdateDestination uses the default value for the destination option, opDestinationSameAsSource.


### -param ppEntry [out]

The updated entry.


#### - destination [in, optional]

This parameter specifies the destination  as a string or as a destination option. Passing a string for the destination implicitly sets the entry's <a href="https://msdn.microsoft.com/93221fe3-bce8-4a36-8e6d-a43d37872295">DestinationOptionSet</a> equal to the DestinationOptionSet property of the <a href="https://msdn.microsoft.com/e9137167-4a2d-4cc4-940e-20f9991c4187">GPMConstants</a> object.  The destination can also be specified by passing the DestinationSameAsSource, DestinationNone, or DestinationByRelativeName properties of the GPMConstants object.


## -returns



<h3>C++</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>JScript</h3>
Returns a reference to a <b>GPMMapEntry</b> object.

<h3>VB</h3>
Returns a reference to a <b>GPMMapEntry</b> object.




## -see-also




<a href="https://msdn.microsoft.com/c3639f07-7c8c-4440-ade4-b58abd2586d6">IGPMMigrationTable</a>
 

 

