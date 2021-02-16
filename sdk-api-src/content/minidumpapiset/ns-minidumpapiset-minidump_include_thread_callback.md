---
UID: NS:minidumpapiset._MINIDUMP_INCLUDE_THREAD_CALLBACK
title: MINIDUMP_INCLUDE_THREAD_CALLBACK (minidumpapiset.h)
description: Contains information for the MiniDumpCallback function when the callback type is IncludeThreadCallback.
helpviewer_keywords: ["*PMINIDUMP_INCLUDE_THREAD_CALLBACK","MINIDUMP_INCLUDE_THREAD_CALLBACK","MINIDUMP_INCLUDE_THREAD_CALLBACK structure","PMINIDUMP_INCLUDE_THREAD_CALLBACK","PMINIDUMP_INCLUDE_THREAD_CALLBACK structure pointer","_MINIDUMP_INCLUDE_THREAD_CALLBACK","_win32_minidump_include_thread_callback_str","base.minidump_include_thread_callback_str","minidumpapiset/MINIDUMP_INCLUDE_THREAD_CALLBACK","minidumpapiset/PMINIDUMP_INCLUDE_THREAD_CALLBACK"]
old-location: base\minidump_include_thread_callback_str.htm
tech.root: Debug
ms.assetid: 4695b739-9af4-4bb8-b7d6-409942bc1932
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_INCLUDE_THREAD_CALLBACK, MINIDUMP_INCLUDE_THREAD_CALLBACK, MINIDUMP_INCLUDE_THREAD_CALLBACK structure, PMINIDUMP_INCLUDE_THREAD_CALLBACK, PMINIDUMP_INCLUDE_THREAD_CALLBACK structure pointer, _MINIDUMP_INCLUDE_THREAD_CALLBACK, _win32_minidump_include_thread_callback_str, base.minidump_include_thread_callback_str, minidumpapiset/MINIDUMP_INCLUDE_THREAD_CALLBACK, minidumpapiset/PMINIDUMP_INCLUDE_THREAD_CALLBACK'
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
req.typenames: MINIDUMP_INCLUDE_THREAD_CALLBACK, *PMINIDUMP_INCLUDE_THREAD_CALLBACK
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_INCLUDE_THREAD_CALLBACK
 - minidumpapiset/_MINIDUMP_INCLUDE_THREAD_CALLBACK
 - PMINIDUMP_INCLUDE_THREAD_CALLBACK
 - minidumpapiset/PMINIDUMP_INCLUDE_THREAD_CALLBACK
 - MINIDUMP_INCLUDE_THREAD_CALLBACK
 - minidumpapiset/MINIDUMP_INCLUDE_THREAD_CALLBACK
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
 - MINIDUMP_INCLUDE_THREAD_CALLBACK
---

# MINIDUMP_INCLUDE_THREAD_CALLBACK structure


## -description

Contains information for the 
<a href="/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine">MiniDumpCallback</a> function when the callback type is 
<b>IncludeThreadCallback</b>.

## -struct-fields

### -field ThreadId

The identifier of the thread.

## -see-also

<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_callback_input">MINIDUMP_CALLBACK_INPUT</a>



<a href="/windows/win32/api/minidumpapiset/ne-minidumpapiset-minidump_callback_type">MINIDUMP_CALLBACK_TYPE</a>



<a href="/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine">MiniDumpCallback</a>