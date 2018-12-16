---
UID: NS:minidumpapiset._MINIDUMP_HANDLE_OBJECT_INFORMATION
title: MINIDUMP_HANDLE_OBJECT_INFORMATION
author: windows-sdk-content
description: Contains object-specific information for a handle.
old-location: base\minidump_handle_object_information.htm
tech.root: debug
ms.assetid: fb79de10-7a98-4a21-b394-63e5279b6681
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MINIDUMP_HANDLE_OBJECT_INFORMATION, MINIDUMP_HANDLE_OBJECT_INFORMATION structure, _MINIDUMP_HANDLE_OBJECT_INFORMATION, base.minidump_handle_object_information, minidumpapiset/MINIDUMP_HANDLE_OBJECT_INFORMATION
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
 - MINIDUMP_HANDLE_OBJECT_INFORMATION
product: Windows
targetos: Windows
req.typenames: MINIDUMP_HANDLE_OBJECT_INFORMATION
req.redist: DbgHelp.dll 6.5 or later
---

# MINIDUMP_HANDLE_OBJECT_INFORMATION structure


## -description


Contains object-specific information for a handle.


## -struct-fields




### -field NextInfoRva

An RVA to a 
<b>MINIDUMP_HANDLE_OBJECT_INFORMATION</b> structure that specifies additional object-specific information. This member is 0 if there are no more elements in the list.


### -field InfoType

The object information type. This member is one of the values from the <a href="https://msdn.microsoft.com/255023e3-0412-42c8-ae80-eba5f00af5ff">MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE</a> enumeration.


### -field SizeOfInfo

The size of the information that follows this member, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/c0678315-391c-4ce9-aa77-a88afccf79d9">MINIDUMP_HANDLE_DESCRIPTOR_2</a>
 

 

