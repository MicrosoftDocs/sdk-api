---
UID: NS:minidumpapiset._MINIDUMP_THREAD_EX_LIST
title: MINIDUMP_THREAD_EX_LIST (minidumpapiset.h)
description: Contains a list of threads. (MINIDUMP_THREAD_EX_LIST)
helpviewer_keywords: ["*PMINIDUMP_THREAD_EX_LIST","MINIDUMP_THREAD_EX_LIST","MINIDUMP_THREAD_EX_LIST structure","PMINIDUMP_THREAD_EX_LIST","PMINIDUMP_THREAD_EX_LIST structure pointer","_MINIDUMP_THREAD_EX_LIST","_win32_minidump_thread_ex_list_str","base.minidump_thread_ex_list_str","minidumpapiset/MINIDUMP_THREAD_EX_LIST","minidumpapiset/PMINIDUMP_THREAD_EX_LIST"]
old-location: base\minidump_thread_ex_list_str.htm
tech.root: Debug
ms.assetid: 653f1079-07c9-43b9-8dfe-05e99b365bdc
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_THREAD_EX_LIST, MINIDUMP_THREAD_EX_LIST, MINIDUMP_THREAD_EX_LIST structure, PMINIDUMP_THREAD_EX_LIST, PMINIDUMP_THREAD_EX_LIST structure pointer, _MINIDUMP_THREAD_EX_LIST, _win32_minidump_thread_ex_list_str, base.minidump_thread_ex_list_str, minidumpapiset/MINIDUMP_THREAD_EX_LIST, minidumpapiset/PMINIDUMP_THREAD_EX_LIST'
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
req.typenames: MINIDUMP_THREAD_EX_LIST, *PMINIDUMP_THREAD_EX_LIST
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_THREAD_EX_LIST
 - minidumpapiset/_MINIDUMP_THREAD_EX_LIST
 - PMINIDUMP_THREAD_EX_LIST
 - minidumpapiset/PMINIDUMP_THREAD_EX_LIST
 - MINIDUMP_THREAD_EX_LIST
 - minidumpapiset/MINIDUMP_THREAD_EX_LIST
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
 - MINIDUMP_THREAD_EX_LIST
---

# MINIDUMP_THREAD_EX_LIST structure


## -description

Contains a list of threads.

## -struct-fields

### -field NumberOfThreads

The number of structures in the <b>Threads</b> array.

### -field Threads

An array of 
<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_thread_ex">MINIDUMP_THREAD_EX</a> structures.

## -see-also

<a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_stream_type">MINIDUMP_STREAM_TYPE</a>



<a href="/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_thread_ex">MINIDUMP_THREAD_EX</a>
