---
UID: NF:werapi.WerUnregisterMemoryBlock
title: WerUnregisterMemoryBlock function
author: windows-sdk-content
description: Removes a memory block from the list of data to be collected during error reporting for the application.
old-location: wer\werunregistermemoryblock.htm
tech.root: wer
ms.assetid: 016800e8-4a03-40f6-9dba-54cd9082eb48
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: WerUnregisterMemoryBlock, WerUnregisterMemoryBlock function [Windows Error Reporting], base.werunregistermemoryblock, wer.werunregistermemoryblock, werapi/WerUnregisterMemoryBlock
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: werapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - API-MS-Win-Core-Windowserrorreporting-l1-1-0.dll
 - KernelBase.dll
api_name:
 - WerUnregisterMemoryBlock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WerUnregisterMemoryBlock function


## -description


Removes a memory block from the list of data to be collected during error reporting for the application.


## -parameters




### -param pvAddress [in]

The starting address of the memory block. This memory block must have been registered using the <a href="https://msdn.microsoft.com/10fa2bf3-ec12-4c7c-b986-9b22cdaa7319">WerRegisterMemoryBlock</a> function.


## -returns



This function returns <b>S_OK</b> on success or an error code on failure, including the following error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WER_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The process state is not valid. For example, the process is in <a href="https://msdn.microsoft.com/9357786c-1992-4e28-ac75-c2dfda1df7f1">application recovery mode</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WER_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The list of registered memory blocks does not contain the specified memory block.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4e28f379-5793-4d76-898e-d87a0291c034">WER Functions</a>



<a href="https://msdn.microsoft.com/10fa2bf3-ec12-4c7c-b986-9b22cdaa7319">WerRegisterMemoryBlock</a>



<a href="https://msdn.microsoft.com/5c076588-779c-4cd2-9fd9-1db3039e37a2">Windows Error Reporting</a>
 

 

