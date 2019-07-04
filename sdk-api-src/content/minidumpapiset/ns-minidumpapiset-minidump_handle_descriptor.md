---
UID: NS:minidumpapiset._MINIDUMP_HANDLE_DESCRIPTOR
title: MINIDUMP_HANDLE_DESCRIPTOR (minidumpapiset.h)
author: windows-sdk-content
description: Contains the state of an individual system handle at the time the minidump was written.
old-location: base\minidump_handle_descriptor_str.htm
tech.root: Debug
ms.assetid: 8387513a-137a-418e-8341-8066965849e6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PMINIDUMP_HANDLE_DESCRIPTOR, MINIDUMP_HANDLE_DESCRIPTOR, MINIDUMP_HANDLE_DESCRIPTOR structure, PMINIDUMP_HANDLE_DESCRIPTOR, PMINIDUMP_HANDLE_DESCRIPTOR structure pointer, _MINIDUMP_HANDLE_DESCRIPTOR, _win32_minidump_handle_descriptor_str, base.minidump_handle_descriptor_str, minidumpapiset/MINIDUMP_HANDLE_DESCRIPTOR, minidumpapiset/PMINIDUMP_HANDLE_DESCRIPTOR"
ms.topic: struct
f1_keywords: 
 - "minidumpapiset/MINIDUMP_HANDLE_DESCRIPTOR"
req.header: minidumpapiset.h
req.include-header: DbgHelp.h
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
 - MINIDUMP_HANDLE_DESCRIPTOR
product: Windows
targetos: Windows
req.typenames: MINIDUMP_HANDLE_DESCRIPTOR, *PMINIDUMP_HANDLE_DESCRIPTOR
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
---

# MINIDUMP_HANDLE_DESCRIPTOR structure


## -description


Contains the state of an individual system handle at the time the minidump was written.


## -struct-fields




### -field Handle

The operating system handle value.


### -field TypeNameRva

An RVA to a 
<a href="https://docs.microsoft.com/windows/desktop/api/minidumpapiset/ns-minidumpapiset-_minidump_string">MINIDUMP_STRING</a> structure that specifies the object type of the handle. This member can be zero.


### -field ObjectNameRva

An RVA to a 
<a href="https://docs.microsoft.com/windows/desktop/api/minidumpapiset/ns-minidumpapiset-_minidump_string">MINIDUMP_STRING</a> structure that specifies the object name of the handle. This member can be zero.


### -field Attributes

The meaning of this member depends on the handle type and the operating system.


### -field GrantedAccess

The meaning of this member depends on the handle type and the operating system.


### -field HandleCount

The meaning of this member depends on the handle type and the operating system.


### -field PointerCount

The meaning of this member depends on the handle type and the operating system.


## -remarks



The first descriptor in the handle data stream follows the header, 
<a href="https://docs.microsoft.com/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_handle_data_stream">MINIDUMP_HANDLE_DATA_STREAM</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_handle_data_stream">MINIDUMP_HANDLE_DATA_STREAM</a>



<a href="https://docs.microsoft.com/windows/desktop/api/minidumpapiset/ns-minidumpapiset-_minidump_string">MINIDUMP_STRING</a>
 

 

