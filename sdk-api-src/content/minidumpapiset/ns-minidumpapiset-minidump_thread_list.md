---
UID: NS:minidumpapiset._MINIDUMP_THREAD_LIST
title: MINIDUMP_THREAD_LIST (minidumpapiset.h)
description: Contains a list of threads. (MINIDUMP_THREAD_LIST)
helpviewer_keywords: ["*PMINIDUMP_THREAD_LIST","MINIDUMP_THREAD_LIST","MINIDUMP_THREAD_LIST structure","PMINIDUMP_THREAD_LIST","PMINIDUMP_THREAD_LIST structure pointer","_MINIDUMP_THREAD_LIST","_win32_minidump_thread_list_str","base.minidump_thread_list_str","minidumpapiset/MINIDUMP_THREAD_LIST","minidumpapiset/PMINIDUMP_THREAD_LIST"]
old-location: base\minidump_thread_list_str.htm
tech.root: Debug
ms.assetid: aa0491d3-e119-41d0-ab53-a108832745d0
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_THREAD_LIST, MINIDUMP_THREAD_LIST, MINIDUMP_THREAD_LIST structure, PMINIDUMP_THREAD_LIST, PMINIDUMP_THREAD_LIST structure pointer, _MINIDUMP_THREAD_LIST, _win32_minidump_thread_list_str, base.minidump_thread_list_str, minidumpapiset/MINIDUMP_THREAD_LIST, minidumpapiset/PMINIDUMP_THREAD_LIST'
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
req.typenames: MINIDUMP_THREAD_LIST, *PMINIDUMP_THREAD_LIST
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_THREAD_LIST
 - minidumpapiset/_MINIDUMP_THREAD_LIST
 - PMINIDUMP_THREAD_LIST
 - minidumpapiset/PMINIDUMP_THREAD_LIST
 - MINIDUMP_THREAD_LIST
 - minidumpapiset/MINIDUMP_THREAD_LIST
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
 - MINIDUMP_THREAD_LIST
---

# MINIDUMP_THREAD_LIST structure


## -description

Contains a list of threads.

## -struct-fields

### -field NumberOfThreads

The number of structures in the <b>Threads</b> array.

### -field Threads

An array of 
<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_thread">MINIDUMP_THREAD</a> structures.

## -see-also

<a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_stream_type">MINIDUMP_STREAM_TYPE</a>



<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_thread">MINIDUMP_THREAD</a>
