---
UID: NS:minidumpapiset._MINIDUMP_MEMORY_INFO_LIST
title: MINIDUMP_MEMORY_INFO_LIST (minidumpapiset.h)
description: Contains a list of memory regions.
helpviewer_keywords: ["*PMINIDUMP_MEMORY_INFO_LIST","MINIDUMP_MEMORY_INFO_LIST","MINIDUMP_MEMORY_INFO_LIST structure","PMINIDUMP_MEMORY_INFO_LIST","PMINIDUMP_MEMORY_INFO_LIST structure pointer","_MINIDUMP_MEMORY_INFO_LIST","base.minidump_memory_info_list_str","minidumpapiset/MINIDUMP_MEMORY_INFO_LIST","minidumpapiset/PMINIDUMP_MEMORY_INFO_LIST"]
old-location: base\minidump_memory_info_list_str.htm
tech.root: Debug
ms.assetid: c1c9a79b-a35a-47e8-be4c-10b3c4ace937
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_MEMORY_INFO_LIST, MINIDUMP_MEMORY_INFO_LIST, MINIDUMP_MEMORY_INFO_LIST structure, PMINIDUMP_MEMORY_INFO_LIST, PMINIDUMP_MEMORY_INFO_LIST structure pointer, _MINIDUMP_MEMORY_INFO_LIST, base.minidump_memory_info_list_str, minidumpapiset/MINIDUMP_MEMORY_INFO_LIST, minidumpapiset/PMINIDUMP_MEMORY_INFO_LIST'
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
targetos: Windows
req.typenames: MINIDUMP_MEMORY_INFO_LIST, *PMINIDUMP_MEMORY_INFO_LIST
req.redist: DbgHelp.dll 6.3 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_MEMORY_INFO_LIST
 - minidumpapiset/_MINIDUMP_MEMORY_INFO_LIST
 - PMINIDUMP_MEMORY_INFO_LIST
 - minidumpapiset/PMINIDUMP_MEMORY_INFO_LIST
 - MINIDUMP_MEMORY_INFO_LIST
 - minidumpapiset/MINIDUMP_MEMORY_INFO_LIST
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
 - MINIDUMP_MEMORY_INFO_LIST
---

# MINIDUMP_MEMORY_INFO_LIST structure


## -description

Contains a list of memory regions.

## -struct-fields

### -field SizeOfHeader

The size of the header data for the stream, in bytes. This is generally <code>sizeof(MINIDUMP_MEMORY_INFO_LIST)</code>.

### -field SizeOfEntry

The size of each entry following the header, in bytes. This is generally <code>sizeof(MINIDUMP_MEMORY_INFO)</code>.

### -field NumberOfEntries

The number of entries in the stream. These are generally  <a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_memory_info">MINIDUMP_MEMORY_INFO</a> structures. The entries follow the header.

## -see-also

<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_memory_info">MINIDUMP_MEMORY_INFO</a>



<a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_stream_type">MINIDUMP_STREAM_TYPE</a>