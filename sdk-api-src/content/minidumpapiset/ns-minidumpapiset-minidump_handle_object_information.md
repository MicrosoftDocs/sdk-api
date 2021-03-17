---
UID: NS:minidumpapiset._MINIDUMP_HANDLE_OBJECT_INFORMATION
title: MINIDUMP_HANDLE_OBJECT_INFORMATION (minidumpapiset.h)
description: Contains object-specific information for a handle.
helpviewer_keywords: ["MINIDUMP_HANDLE_OBJECT_INFORMATION","MINIDUMP_HANDLE_OBJECT_INFORMATION structure","_MINIDUMP_HANDLE_OBJECT_INFORMATION","base.minidump_handle_object_information","minidumpapiset/MINIDUMP_HANDLE_OBJECT_INFORMATION"]
old-location: base\minidump_handle_object_information.htm
tech.root: Debug
ms.assetid: fb79de10-7a98-4a21-b394-63e5279b6681
ms.date: 12/05/2018
ms.keywords: MINIDUMP_HANDLE_OBJECT_INFORMATION, MINIDUMP_HANDLE_OBJECT_INFORMATION structure, _MINIDUMP_HANDLE_OBJECT_INFORMATION, base.minidump_handle_object_information, minidumpapiset/MINIDUMP_HANDLE_OBJECT_INFORMATION
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
targetos: Windows
req.typenames: MINIDUMP_HANDLE_OBJECT_INFORMATION
req.redist: DbgHelp.dll 6.5 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_HANDLE_OBJECT_INFORMATION
 - minidumpapiset/_MINIDUMP_HANDLE_OBJECT_INFORMATION
 - MINIDUMP_HANDLE_OBJECT_INFORMATION
 - minidumpapiset/MINIDUMP_HANDLE_OBJECT_INFORMATION
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_HANDLE_OBJECT_INFORMATION
---

# MINIDUMP_HANDLE_OBJECT_INFORMATION structure


## -description

Contains object-specific information for a handle.

## -struct-fields

### -field NextInfoRva

An RVA to a 
<b>MINIDUMP_HANDLE_OBJECT_INFORMATION</b> structure that specifies additional object-specific information. This member is 0 if there are no more elements in the list.

### -field InfoType

The object information type. This member is one of the values from the <a href="/windows/win32/api/minidumpapiset/ne-minidumpapiset-minidump_handle_object_information_type">MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE</a> enumeration.

### -field SizeOfInfo

The size of the information that follows this member, in bytes.

## -see-also

<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_handle_descriptor_2">MINIDUMP_HANDLE_DESCRIPTOR_2</a>

