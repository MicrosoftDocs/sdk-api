---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _THREAD_WRITE_FLAGS enumeration


## -description


Identifies the type of thread information that will be written to the minidump file by the 
<a href="https://msdn.microsoft.com/b476023d-0e93-4d76-9ba8-ce5766c9ac51">MiniDumpWriteDump</a> function.


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

When the minidump type includes <b>MiniDumpWithThreadInfo</b>, this flag is set. The callback function can clear this flag to control which threads provide thread state information in the minidump file. For more information, see <a href="https://msdn.microsoft.com/855bbccb-a7c8-4744-b314-8692f785b1c0">MINIDUMP_THREAD_INFO</a>.

<b>DbgHelp 6.1 and earlier:  </b>This value is not supported.


## -see-also




<a href="https://msdn.microsoft.com/57949087-0f22-40c8-ab56-326a8304c310">MINIDUMP_CALLBACK_OUTPUT</a>



<a href="https://msdn.microsoft.com/b476023d-0e93-4d76-9ba8-ce5766c9ac51">MiniDumpWriteDump</a>
 

 

