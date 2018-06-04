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

# _MINIDUMP_HANDLE_DESCRIPTOR_2 structure


## -description


Describes the state of an individual system handle at the time the minidump was written.


## -struct-fields




### -field Handle

The operating system handle value.


### -field TypeNameRva

An RVA to a 
<a href="https://msdn.microsoft.com/b90b2b29-9d39-4a73-b5fb-bb6e04c94811">MINIDUMP_STRING</a> structure that specifies the object type of the handle. This member can be zero.


### -field ObjectNameRva

An RVA to a 
<a href="https://msdn.microsoft.com/b90b2b29-9d39-4a73-b5fb-bb6e04c94811">MINIDUMP_STRING</a> structure that specifies the object name of the handle. This member can be 0.


### -field Attributes

The meaning of this member depends on the handle type and the operating system.


### -field GrantedAccess

The meaning of this member depends on the handle type and the operating system.


### -field HandleCount

The meaning of this member depends on the handle type and the operating system.


### -field PointerCount

The meaning of this member depends on the handle type and the operating system.


### -field ObjectInfoRva

An RVA to a 
<a href="https://msdn.microsoft.com/fb79de10-7a98-4a21-b394-63e5279b6681">MINIDUMP_HANDLE_OBJECT_INFORMATION</a> structure that specifies object-specific information. This member can be 0 if there is no extra information.


### -field Reserved0

Reserved for future use; must be zero.


## -remarks



The first descriptor in the handle data stream follows the header, 
<a href="https://msdn.microsoft.com/5674df6b-77e0-4bca-8349-8217388902ed">MINIDUMP_HANDLE_DATA_STREAM</a>.




## -see-also




<a href="https://msdn.microsoft.com/5674df6b-77e0-4bca-8349-8217388902ed">MINIDUMP_HANDLE_DATA_STREAM</a>



<a href="https://msdn.microsoft.com/fb79de10-7a98-4a21-b394-63e5279b6681">MINIDUMP_HANDLE_OBJECT_INFORMATION</a>



<a href="https://msdn.microsoft.com/b90b2b29-9d39-4a73-b5fb-bb6e04c94811">MINIDUMP_STRING</a>
 

 

