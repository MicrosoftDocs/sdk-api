---
UID: NS:minidumpapiset._MINIDUMP_HANDLE_DESCRIPTOR_2
title: MINIDUMP_HANDLE_DESCRIPTOR_2 (minidumpapiset.h)
author: windows-sdk-content
description: Describes the state of an individual system handle at the time the minidump was written.
old-location: base\minidump_handle_descriptor_2.htm
tech.root: Debug
ms.assetid: c0678315-391c-4ce9-aa77-a88afccf79d9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PMINIDUMP_HANDLE_DESCRIPTOR_2, *PMINIDUMP_HANDLE_DESCRIPTOR_N, MINIDUMP_HANDLE_DESCRIPTOR_2, MINIDUMP_HANDLE_DESCRIPTOR_2 structure, MINIDUMP_HANDLE_DESCRIPTOR_N, PMINIDUMP_HANDLE_DESCRIPTOR_2, PMINIDUMP_HANDLE_DESCRIPTOR_2 structure pointer, _MINIDUMP_HANDLE_DESCRIPTOR_2, base.minidump_handle_descriptor_2, minidumpapiset/MINIDUMP_HANDLE_DESCRIPTOR_2, minidumpapiset/PMINIDUMP_HANDLE_DESCRIPTOR_2"
ms.topic: struct
req.header: minidumpapiset.h
req.include-header: Dbghelp.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_HANDLE_DESCRIPTOR_2
product: Windows
targetos: Windows
req.typenames: MINIDUMP_HANDLE_DESCRIPTOR_2, *PMINIDUMP_HANDLE_DESCRIPTOR_2
req.redist: DbgHelp.dll 6.5 or later
ms.custom: 19H1
---

# MINIDUMP_HANDLE_DESCRIPTOR_2 structure


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
<a href="https://msdn.microsoft.com/en-us/library/ms680375(v=VS.85).aspx">MINIDUMP_HANDLE_OBJECT_INFORMATION</a> structure that specifies object-specific information. This member can be 0 if there is no extra information.


### -field Reserved0

Reserved for future use; must be zero.


## -remarks



The first descriptor in the handle data stream follows the header, 
<a href="https://msdn.microsoft.com/en-us/library/ms680372(v=VS.85).aspx">MINIDUMP_HANDLE_DATA_STREAM</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms680372(v=VS.85).aspx">MINIDUMP_HANDLE_DATA_STREAM</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680375(v=VS.85).aspx">MINIDUMP_HANDLE_OBJECT_INFORMATION</a>



<a href="https://msdn.microsoft.com/b90b2b29-9d39-4a73-b5fb-bb6e04c94811">MINIDUMP_STRING</a>
 

 

