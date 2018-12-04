---
UID: NF:werapi.WerRegisterMemoryBlock
title: WerRegisterMemoryBlock function
author: windows-sdk-content
description: Registers a memory block to be collected when WER creates an error report.
old-location: wer\werregistermemoryblock.htm
tech.root: wer
ms.assetid: 10fa2bf3-ec12-4c7c-b986-9b22cdaa7319
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: WerRegisterMemoryBlock, WerRegisterMemoryBlock function [Windows Error Reporting], base.werregistermemoryblock, wer.werregistermemoryblock, werapi/WerRegisterMemoryBlock
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
 - WerRegisterMemoryBlock
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WerRegisterMemoryBlock function


## -description


Registers a memory block to be collected when WER creates an error report.


## -parameters




### -param pvAddress [in]

The starting address of the memory block.


### -param dwSize [in]

The size of the memory block, in bytes. The maximum value for this parameter is WER_MAX_MEM_BLOCK_SIZE bytes.


## -returns



This function returns <b>S_OK</b> on success or an error code on failure, including the following error codes.

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
<dt><b>HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</b></dt>
</dl>
</td>
<td width="60%">
The number of registered memory blocks and files exceeds the limit.

</td>
</tr>
</table>
 




## -remarks



Memory registered with this function is only added to heap or larger dump files. This memory is never added to mini dumps or smaller dump files.

For crashes and no response, the operating system automatically provides error reporting (you do not need to provide any error reporting code in your application). If you use this function to register a memory block, the operating system will add the memory block information to the dump file at the time of the crash or non-response. The memory block is added to the dump file for the report only when additional data is requested by the server.

For generic event reporting, the application has to call the WER generic event reporting functions directly. To add the memory block to a generic report, call the <a href="https://msdn.microsoft.com/b40dac44-f7c5-43f0-876d-6f97c26bf461">WerReportAddDump</a> function and then call the <a href="https://msdn.microsoft.com/1433862e-5cf6-4d31-9fd9-137b7b86ec57">WerReportSubmit</a> function and specify the  WER_SUBMIT_ADD_REGISTERED_DATA flag.


To remove the block from this list, call the <a href="https://msdn.microsoft.com/016800e8-4a03-40f6-9dba-54cd9082eb48">WerUnregisterMemoryBlock</a> function.




## -see-also




<a href="https://msdn.microsoft.com/4e28f379-5793-4d76-898e-d87a0291c034">WER Functions</a>



<a href="https://msdn.microsoft.com/016800e8-4a03-40f6-9dba-54cd9082eb48">WerUnregisterMemoryBlock</a>



<a href="https://msdn.microsoft.com/5c076588-779c-4cd2-9fd9-1db3039e37a2">Windows Error Reporting</a>
 

 

