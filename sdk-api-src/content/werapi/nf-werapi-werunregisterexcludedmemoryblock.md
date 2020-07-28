---
UID: NF:werapi.WerUnregisterExcludedMemoryBlock
title: WerUnregisterExcludedMemoryBlock function (werapi.h)
description: Removes a memory block that was previously marked as excluded (it will again be included in error reports).
helpviewer_keywords: ["WerUnregisterExcludedMemoryBlock","WerUnregisterExcludedMemoryBlock function [Windows Error Reporting]","wer.werunregisterexcludedmemoryblock","werapi/WerUnregisterExcludedMemoryBlock"]
old-location: wer\werunregisterexcludedmemoryblock.htm
tech.root: wer
ms.assetid: 99FF746E-8EFC-47DB-AEE6-EC46F7BC7F0B
ms.date: 12/05/2018
ms.keywords: WerUnregisterExcludedMemoryBlock, WerUnregisterExcludedMemoryBlock function [Windows Error Reporting], wer.werunregisterexcludedmemoryblock, werapi/WerUnregisterExcludedMemoryBlock
f1_keywords:
- werapi/WerUnregisterExcludedMemoryBlock
dev_langs:
- c++
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
- WerUnregisterExcludedMemoryBlock
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WerUnregisterExcludedMemoryBlock function


## -description


Removes a memory block that was  previously marked as excluded (it will again be included in error reports).


## -parameters




### -param address

The starting address of the memory block. This memory block must have been registered using the <a href="https://docs.microsoft.com/windows/desktop/api/werapi/nf-werapi-werregisterexcludedmemoryblock">WerRegisterExcludedMemoryBlock</a> function.


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
The process state is not valid. For example, the process is in <a href="https://docs.microsoft.com/windows/desktop/wsw/portal">application recovery mode</a>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wer/wer-functions">WER Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/werapi/nf-werapi-werregisterexcludedmemoryblock">WerRegisterExcludedMemoryBlock</a>



<a href="https://docs.microsoft.com/windows/desktop/wer/windows-error-reporting">Windows Error Reporting</a>
 

 

