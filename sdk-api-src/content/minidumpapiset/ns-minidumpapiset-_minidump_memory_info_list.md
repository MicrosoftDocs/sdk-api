---
UID: NS:minidumpapiset._MINIDUMP_MEMORY_INFO_LIST
title: "_MINIDUMP_MEMORY_INFO_LIST"
author: windows-sdk-content
description: Contains a list of memory regions.
old-location: base\minidump_memory_info_list_str.htm
old-project: debug
ms.assetid: c1c9a79b-a35a-47e8-be4c-10b3c4ace937
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PMINIDUMP_MEMORY_INFO_LIST, MINIDUMP_MEMORY_INFO_LIST, MINIDUMP_MEMORY_INFO_LIST structure, PMINIDUMP_MEMORY_INFO_LIST, PMINIDUMP_MEMORY_INFO_LIST structure pointer, _MINIDUMP_MEMORY_INFO_LIST, base.minidump_memory_info_list_str, minidumpapiset/MINIDUMP_MEMORY_INFO_LIST, minidumpapiset/PMINIDUMP_MEMORY_INFO_LIST"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: MINIDUMP_MEMORY_INFO_LIST, *PMINIDUMP_MEMORY_INFO_LIST
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - minidumpapiset.h
api_name:
 - MINIDUMP_MEMORY_INFO_LIST
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MINIDUMP_MEMORY_INFO_LIST structure


## -description


Contains a list of memory regions.


## -struct-fields




### -field SizeOfHeader

The size of the header data for the stream, in bytes. This is generally <code>sizeof(MINIDUMP_MEMORY_INFO_LIST)</code>.


### -field SizeOfEntry

The size of each entry following the header, in bytes. This is generally <code>sizeof(MINIDUMP_MEMORY_INFO)</code>.


### -field NumberOfEntries

The number of entries in the stream. These are generally  <a href="https://msdn.microsoft.com/e9a797b9-5cad-48c0-bb33-ca9c13de8239">MINIDUMP_MEMORY_INFO</a> structures. The entries follow the header.


## -see-also




<a href="https://msdn.microsoft.com/e9a797b9-5cad-48c0-bb33-ca9c13de8239">MINIDUMP_MEMORY_INFO</a>



<a href="https://msdn.microsoft.com/495136a0-2fed-47ca-8233-7e813b43b82f">MINIDUMP_STREAM_TYPE</a>
 

 

