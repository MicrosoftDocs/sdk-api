---
UID: NF:enclaveapi.DeleteEnclave
title: DeleteEnclave function
author: windows-sdk-content
description: Deletes the specified enclave.
old-location: base\deleteenclave.htm
tech.root: memory
ms.assetid: 04FCD129-3A3B-40EA-AD62-01C674CF2E61
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: DeleteEnclave, DeleteEnclave function, base.deleteenclave, enclaveapi/DeleteEnclave
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: enclaveapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Vertdll.lib
req.dll: Vertdll.dll; Api-ms-win-core-enclave-l1-1-0.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Vertdll.dll
 - api-ms-win-core-enclave-l1-1-0.dll
api_name:
 - DeleteEnclave
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DeleteEnclave function


## -description


Deletes the specified enclave.


## -parameters




### -param lpAddress [in]

The base address of the enclave that you want to delete. 


## -returns



<b>TRUE</b> if the enclave was deleted successfully; otherwise <b>FALSE</b>. To get extended error information, 
       call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 

For a list of common error codes, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>. The following error codes also apply for this function.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ENCLAVE_NOT_TERMINATED</b></dt>
</dl>
</td>
<td width="60%">
The execution of threads running with the enclave was not ended, because either <a href="https://msdn.microsoft.com/D2BAF02F-AE05-43F2-BDB1-013EAF3AC653">TerminateEnclave</a> was not called, or the execution of the threads has not yet ended in response to an earlier call to <b>TerminateEnclave</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2193AE42-D9CC-4A9C-8676-7DE432ED58C3">CreateEnclave</a>
 

 

