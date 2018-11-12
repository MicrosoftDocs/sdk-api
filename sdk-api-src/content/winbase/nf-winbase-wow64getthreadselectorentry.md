---
UID: NF:winbase.Wow64GetThreadSelectorEntry
title: Wow64GetThreadSelectorEntry function
author: windows-sdk-content
description: Retrieves a descriptor table entry for the specified selector and WOW64 thread.
old-location: base\wow64getthreadselectorentry.htm
tech.root: debug
ms.assetid: 68393913-6725-4cc6-90b9-57da2a96c91e
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: Wow64GetThreadSelectorEntry, Wow64GetThreadSelectorEntry function, base.wow64getthreadselectorentry, winbase/Wow64GetThreadSelectorEntry
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
api_name:
 - Wow64GetThreadSelectorEntry
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# Wow64GetThreadSelectorEntry function


## -description


Retrieves a descriptor table entry for the specified selector and WOW64 thread. 


## -parameters




### -param hThread [in]

A handle to the thread containing the
        specified selector.  The handle must have been created with
        THREAD_QUERY_INFORMATION access to the thread. For more information, see 
<a href="https://msdn.microsoft.com/72709446-5c59-4fac-8dc8-7912906ecc85">Thread Security and Access Rights</a>.


### -param dwSelector [in]

The global or local selector value to look up in the thread's descriptor tables.


### -param lpSelectorEntry [out]

A pointer to a 
<a href="https://msdn.microsoft.com/a571cd2f-0873-4ad5-bcb8-c0da2d47a820">WOW64_LDT_ENTRY</a> structure that receives a copy of the descriptor table entry if the specified selector has an entry in the specified thread's descriptor table. This information can be used to convert a segment-relative address to a linear virtual address.


## -returns



If the function succeeds, the return value is nonzero. In that case, the structure pointed to by the <i>lpSelectorEntry</i> parameter receives a copy of the specified descriptor table entry.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>Wow64GetThreadSelectorEntry</b> function is functional only on 64-bit systems and can be called only by 64-bit processes. If this function is called by a 32-bit process, the function fails with ERROR_NOT_SUPPORTED. A 32-bit process should use the <a href="https://msdn.microsoft.com/9bf6f7b1-7a30-4398-a12a-b1de986f860d">GetThreadSelectorEntry</a> function instead. 

Debuggers use this function to convert segment-relative addresses to linear virtual addresses. The 
<a href="https://msdn.microsoft.com/8774e145-ee7f-44de-85db-0445b905f986">ReadProcessMemory</a> and 
<a href="https://msdn.microsoft.com/9cd91f1c-58ce-4adc-b027-45748543eb06">WriteProcessMemory</a> functions use linear virtual addresses.



