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



