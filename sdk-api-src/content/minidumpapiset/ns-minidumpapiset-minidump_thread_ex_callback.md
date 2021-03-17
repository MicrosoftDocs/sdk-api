---
UID: NS:minidumpapiset._MINIDUMP_THREAD_EX_CALLBACK
title: MINIDUMP_THREAD_EX_CALLBACK (minidumpapiset.h)
description: Contains extended thread information for the MiniDumpCallback function when the callback type is ThreadExCallback.
helpviewer_keywords: ["*PMINIDUMP_THREAD_EX_CALLBACK","MINIDUMP_THREAD_EX_CALLBACK","MINIDUMP_THREAD_EX_CALLBACK structure","PMINIDUMP_THREAD_EX_CALLBACK","PMINIDUMP_THREAD_EX_CALLBACK structure pointer","_MINIDUMP_THREAD_EX_CALLBACK","_win32_minidump_thread_ex_callback_str","base.minidump_thread_ex_callback_str","minidumpapiset/MINIDUMP_THREAD_EX_CALLBACK","minidumpapiset/PMINIDUMP_THREAD_EX_CALLBACK"]
old-location: base\minidump_thread_ex_callback_str.htm
tech.root: Debug
ms.assetid: a81856df-14a3-42bc-89dc-9796c7b252be
ms.date: 12/05/2018
ms.keywords: '*PMINIDUMP_THREAD_EX_CALLBACK, MINIDUMP_THREAD_EX_CALLBACK, MINIDUMP_THREAD_EX_CALLBACK structure, PMINIDUMP_THREAD_EX_CALLBACK, PMINIDUMP_THREAD_EX_CALLBACK structure pointer, _MINIDUMP_THREAD_EX_CALLBACK, _win32_minidump_thread_ex_callback_str, base.minidump_thread_ex_callback_str, minidumpapiset/MINIDUMP_THREAD_EX_CALLBACK, minidumpapiset/PMINIDUMP_THREAD_EX_CALLBACK'
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
req.typenames: MINIDUMP_THREAD_EX_CALLBACK, *PMINIDUMP_THREAD_EX_CALLBACK
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _MINIDUMP_THREAD_EX_CALLBACK
 - minidumpapiset/_MINIDUMP_THREAD_EX_CALLBACK
 - PMINIDUMP_THREAD_EX_CALLBACK
 - minidumpapiset/PMINIDUMP_THREAD_EX_CALLBACK
 - MINIDUMP_THREAD_EX_CALLBACK
 - minidumpapiset/MINIDUMP_THREAD_EX_CALLBACK
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
 - MINIDUMP_THREAD_EX_CALLBACK
---

# MINIDUMP_THREAD_EX_CALLBACK structure


## -description

Contains extended thread information for the 
<a href="/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine">MiniDumpCallback</a> function when the callback type is 
<a href="/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_callback_type">ThreadExCallback</a>.

## -struct-fields

### -field ThreadId

The identifier of the thread.

### -field ThreadHandle

A handle to the thread

### -field Pad

### -field Context

A 
<a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a> structure that contains the processor-specific data.

### -field SizeOfContext

The size of the returned processor-specific data in the <b>Context</b> member, in bytes.

### -field StackBase

The base address of the thread stack.

### -field StackEnd

The ending address of the thread stack.

### -field BackingStoreBase

<b>Intel Itanium:  </b>The base address of the thread backing store.

### -field BackingStoreEnd

<b>Intel Itanium:  </b>The ending address of the thread backing store.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-arm64_nt_context">CONTEXT</a>



<a href="/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_callback_input">MINIDUMP_CALLBACK_INPUT</a>



<a href="/windows/desktop/api/minidumpapiset/nc-minidumpapiset-minidump_callback_routine">MiniDumpCallback</a>