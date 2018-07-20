---
UID: NF:werapi.WerUnregisterExcludedMemoryBlock
title: WerUnregisterExcludedMemoryBlock function
author: windows-sdk-content
description: Removes a memory block that was previously marked as excluded (it will again be included in error reports).
old-location: wer\werunregisterexcludedmemoryblock.htm
old-project: wer
ms.assetid: 99FF746E-8EFC-47DB-AEE6-EC46F7BC7F0B
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: WerUnregisterExcludedMemoryBlock, WerUnregisterExcludedMemoryBlock function [Windows Error Reporting], wer.werunregisterexcludedmemoryblock, werapi/WerUnregisterExcludedMemoryBlock
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: werapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WEB_SOCKET_PROPERTY, *PWEB_SOCKET_PROPERTY
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
 - WerUnregisterExcludedMemoryBlock
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WerUnregisterExcludedMemoryBlock function


## -description


Removes a memory block that was  previously marked as excluded (it will again be included in error reports).


## -parameters




### -param address

The starting address of the memory block. This memory block must have been registered using the <a href="https://msdn.microsoft.com/6CDA8EDD-C8A5-471D-9716-3AB29E571133">WerRegisterExcludedMemoryBlock</a> function.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4e28f379-5793-4d76-898e-d87a0291c034">WER Functions</a>



<a href="https://msdn.microsoft.com/6CDA8EDD-C8A5-471D-9716-3AB29E571133">WerRegisterExcludedMemoryBlock</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/jj242491">Windows Error Reporting</a>
 

 

