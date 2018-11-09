---
UID: NF:ntsecapi.LsaFreeMemory
title: LsaFreeMemory function
author: windows-sdk-content
description: The LsaFreeMemory function frees memory allocated for an output buffer by an LSA function call.
old-location: security\lsafreememory.htm
tech.root: secmgmt
ms.assetid: 6eb3d18f-c54c-4e51-8a4b-b7a3f930cfa9
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: LsaFreeMemory, LsaFreeMemory function [Security], _lsa_lsafreememory, ntsecapi/LsaFreeMemory, security.lsafreememory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-Security-lsapolicy-l1-1-0.dll
 - sechost.dll
 - API-MS-Win-Security-LSAPolicy-L1-1-1.dll
api_name:
 - LsaFreeMemory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LsaFreeMemory function


## -description


The <b>LsaFreeMemory</b> function frees memory allocated for an output buffer by an LSA function call. LSA functions that return variable-length output buffers always allocate the buffer on behalf of the caller. The caller must free this memory by passing the returned buffer pointer to <b>LsaFreeMemory</b> when the memory is no longer required.


## -parameters




### -param Buffer [in]

Pointer to memory buffer that was allocated by an LSA function call. If <b>LsaFreeMemory</b> is successful, this buffer is freed.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code, which can be the following value or one of the 
<a href="https://msdn.microsoft.com/en-us/library/ms721859(v=VS.85).aspx">LSA Policy Function Return Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_UNSUCCESSFUL</b></dt>
</dl>
</td>
<td width="60%">
Memory could not be freed because it was not allocated by an LSA function call.

</td>
</tr>
</table>
 

You can use the 
<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a> function to convert the NTSTATUS code to a Windows error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms721859(v=VS.85).aspx">LSA Policy Function Return Values</a>



<a href="https://msdn.microsoft.com/fa91794c-c502-4b36-84cc-a8d77c8e9d9f">LsaNtStatusToWinError</a>
 

 

