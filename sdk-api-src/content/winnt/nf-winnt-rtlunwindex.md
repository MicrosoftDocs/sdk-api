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

# RtlUnwindEx function


## -description


Initiates an unwind of 
   procedure call frames.


## -parameters




### -param TargetFrame [in, optional]

A pointer to the call frame that is the target of the unwind. If this parameter is <b>NULL</b>, the function 
      performs an exit unwind.


### -param TargetIp [in, optional]

The continuation address of the unwind. This parameter is ignored if <i>TargetFrame</i> is 
      <b>NULL</b>.


### -param ExceptionRecord [in, optional]

A pointer to an <a href="https://msdn.microsoft.com/85a64178-bdcb-4293-9363-289c654730a2">EXCEPTION_RECORD</a> structure.


### -param ReturnValue [in]

A value to be placed in the integer function return register before continuing execution.


### -param ContextRecord

TBD


### -param HistoryTable [in, optional]

A pointer to the unwind history table. This structure is processor specific. For definitions of this 
      structure, see Winternl.h.


#### - OriginalContext [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">CONTEXT</a> structure that stores context 
      during the unwind operation.


## -returns



This function does not return a value.




## -remarks



The <b>FRAME_POINTERS</b> structure is defined as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>typedef struct _FRAME_POINTERS {
    ULONGLONG MemoryStackFp;
    ULONGLONG BackingStoreFp;
} FRAME_POINTERS, *PFRAME_POINTERS;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">CONTEXT</a>



<a href="https://msdn.microsoft.com/85a64178-bdcb-4293-9363-289c654730a2">EXCEPTION_RECORD</a>
 

 

