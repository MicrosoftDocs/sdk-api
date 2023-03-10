---
UID: NS:minidumpapiset._MINIDUMP_THREAD_INFO_LIST
title: MINIDUMP_THREAD_INFO_LIST (minidumpapiset.h)
description: Contains a list of threads. (MINIDUMP_THREAD_INFO_LIST)
helpviewer_keywords: ["*PMINIDUMP_THREAD_INFO_LIST","MINIDUMP_THREAD_INFO_LIST","MINIDUMP_THREAD_INFO_LIST structure","PMINIDUMP_THREAD_INFO_LIST","PMINIDUMP_THREAD_INFO_LIST structure pointer","_MINIDUMP_THREAD_INFO_LIST","base.minidump_thread_info_list_str","minidumpapiset/MINIDUMP_THREAD_INFO_LIST","minidumpapiset/PMINIDUMP_THREAD_INFO_LIST"]
old-location: base\minidump_thread_info_list_str.htm
tech.root: Debug
ms.assetid: ee02a8fa-c81d-4b23-b8a2-6ff31cdaf3de
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_THREAD_INFO_LIST, MINIDUMP_THREAD_INFO_LIST, MINIDUMP_THREAD_INFO_LIST structure, PMINIDUMP_THREAD_INFO_LIST, PMINIDUMP_THREAD_INFO_LIST structure pointer, _MINIDUMP_THREAD_INFO_LIST, base.minidump_thread_info_list_str, minidumpapiset/MINIDUMP_THREAD_INFO_LIST, minidumpapiset/PMINIDUMP_THREAD_INFO_LIST'
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
req.typenames: MINIDUMP_THREAD_INFO_LIST, *PMINIDUMP_THREAD_INFO_LIST
req.redist: DbgHelp.dll 6.3 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_THREAD_INFO_LIST
 - minidumpapiset/_MINIDUMP_THREAD_INFO_LIST
 - PMINIDUMP_THREAD_INFO_LIST
 - minidumpapiset/PMINIDUMP_THREAD_INFO_LIST
 - MINIDUMP_THREAD_INFO_LIST
 - minidumpapiset/MINIDUMP_THREAD_INFO_LIST
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
 - MINIDUMP_THREAD_INFO_LIST
---

# MINIDUMP_THREAD_INFO_LIST structure


## -description

Contains a list of threads.

## -struct-fields

### -field SizeOfHeader

The size of the header data for the stream, in bytes. This is generally 
      <code>sizeof(MINIDUMP_THREAD_INFO_LIST)</code>.

### -field SizeOfEntry

The size of each entry following the header, in bytes. This is generally 
      <code>sizeof(MINIDUMP_THREAD_INFO)</code>.

### -field NumberOfEntries

The number of entries in the stream. These are generally 
      <a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_thread_info">MINIDUMP_THREAD_INFO</a> structures. The entries 
      follow the header.

## -see-also

<a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_stream_type">MINIDUMP_STREAM_TYPE</a>



<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_thread_info">MINIDUMP_THREAD_INFO</a>
