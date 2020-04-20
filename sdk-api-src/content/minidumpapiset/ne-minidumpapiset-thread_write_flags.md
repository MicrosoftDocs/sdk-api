---
UID: NE:minidumpapiset._THREAD_WRITE_FLAGS
title: THREAD_WRITE_FLAGS (minidumpapiset.h)
description: Identifies the type of thread information that will be written to the minidump file by the MiniDumpWriteDump function.helpviewer_keywords: ["THREAD_WRITE_FLAGS","THREAD_WRITE_FLAGS enumeration","ThreadWriteBackingStore","ThreadWriteContext","ThreadWriteInstructionWindow","ThreadWriteStack","ThreadWriteThread","ThreadWriteThreadData","ThreadWriteThreadInfo","_win32_thread_write_flags","base.thread_write_flags","minidumpapiset/THREAD_WRITE_FLAGS","minidumpapiset/ThreadWriteBackingStore","minidumpapiset/ThreadWriteContext","minidumpapiset/ThreadWriteInstructionWindow","minidumpapiset/ThreadWriteStack","minidumpapiset/ThreadWriteThread","minidumpapiset/ThreadWriteThreadData","minidumpapiset/ThreadWriteThreadInfo"]
old-location: base\thread_write_flags.htm
tech.root: Debug
ms.assetid: b2d933c0-5e52-4078-82ea-844c2415eb45
ms.date: 12/05/2018
ms.keywords: THREAD_WRITE_FLAGS, THREAD_WRITE_FLAGS enumeration, ThreadWriteBackingStore, ThreadWriteContext, ThreadWriteInstructionWindow, ThreadWriteStack, ThreadWriteThread, ThreadWriteThreadData, ThreadWriteThreadInfo, _win32_thread_write_flags, base.thread_write_flags, minidumpapiset/THREAD_WRITE_FLAGS, minidumpapiset/ThreadWriteBackingStore, minidumpapiset/ThreadWriteContext, minidumpapiset/ThreadWriteInstructionWindow, minidumpapiset/ThreadWriteStack, minidumpapiset/ThreadWriteThread, minidumpapiset/ThreadWriteThreadData, minidumpapiset/ThreadWriteThreadInfo
f1_keywords:
- minidumpapiset/THREAD_WRITE_FLAGS
dev_langs:
- c++
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
- THREAD_WRITE_FLAGS
targetos: Windows
req.typenames: THREAD_WRITE_FLAGS
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
---

# THREAD_WRITE_FLAGS enumeration


## -description


Identifies the type of thread information that will be written to the minidump file by the 
<a href="https://docs.microsoft.com/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump">MiniDumpWriteDump</a> function.


## -enum-fields




### -field ThreadWriteThread

Only basic thread information will be written to the minidump file.


### -field ThreadWriteStack

Basic thread and thread stack information will be written to the minidump file.


### -field ThreadWriteContext

The entire thread context will be written to the minidump file.


### -field ThreadWriteBackingStore

<b>Intel Itanium:  </b>The backing store memory of every thread will be written to the minidump file.


### -field ThreadWriteInstructionWindow

A small amount of memory surrounding each thread's instruction pointer will be written to the minidump file. This allows instructions near a thread's instruction pointer to be disassembled even if an executable image matching the module cannot be found.


### -field ThreadWriteThreadData

When the minidump type includes <b>MiniDumpWithProcessThreadData</b>, this flag is set. The callback function can clear this flag to control which threads provide complete thread data in the minidump file.

<b>DbgHelp 5.1:  </b>This value is not supported.


### -field ThreadWriteThreadInfo

When the minidump type includes <b>MiniDumpWithThreadInfo</b>, this flag is set. The callback function can clear this flag to control which threads provide thread state information in the minidump file. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/minidumpapiset/ns-minidumpapiset-minidump_thread_info">MINIDUMP_THREAD_INFO</a>.

<b>DbgHelp 6.1 and earlier:  </b>This value is not supported.


## -see-also




<a href="https://docs.microsoft.com/windows/win32/api/minidumpapiset/ns-minidumpapiset-minidump_callback_output">MINIDUMP_CALLBACK_OUTPUT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/minidumpapiset/nf-minidumpapiset-minidumpwritedump">MiniDumpWriteDump</a>
 

 

