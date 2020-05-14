---
UID: NF:werapi.WerUnregisterMemoryBlock
title: WerUnregisterMemoryBlock function (werapi.h)
description: Removes a memory block from the list of data to be collected during error reporting for the application.helpviewer_keywords: ["WerUnregisterMemoryBlock","WerUnregisterMemoryBlock function [Windows Error Reporting]","base.werunregistermemoryblock","wer.werunregistermemoryblock","werapi/WerUnregisterMemoryBlock"]
old-location: wer\werunregistermemoryblock.htm
tech.root: wer
ms.assetid: 016800e8-4a03-40f6-9dba-54cd9082eb48
ms.date: 12/05/2018
ms.keywords: WerUnregisterMemoryBlock, WerUnregisterMemoryBlock function [Windows Error Reporting], base.werunregistermemoryblock, wer.werunregistermemoryblock, werapi/WerUnregisterMemoryBlock
f1_keywords:
- werapi/WerUnregisterMemoryBlock
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WerUnregisterMemoryBlock function


## -description


Removes a memory block from the list of data to be collected during error reporting for the application.


## -parameters




### -param pvAddress [in]

The starting address of the memory block. This memory block must have been registered using the <a href="https://docs.microsoft.com/windows/desktop/api/werapi/nf-werapi-werregistermemoryblock">WerRegisterMemoryBlock</a> function.


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




<a href="https://docs.microsoft.com/windows/desktop/wer/wer-functions">WER Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/werapi/nf-werapi-werregistermemoryblock">WerRegisterMemoryBlock</a>



<a href="https://docs.microsoft.com/windows/desktop/wer/windows-error-reporting">Windows Error Reporting</a>
 

 

