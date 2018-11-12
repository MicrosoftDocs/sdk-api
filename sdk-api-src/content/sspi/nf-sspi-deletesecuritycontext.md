---
UID: NF:sspi.DeleteSecurityContext
title: DeleteSecurityContext function
author: windows-sdk-content
description: Deletes the local data structures associated with the specified security context initiated by a previous call to the InitializeSecurityContext (General) function or the AcceptSecurityContext (General) function.
old-location: security\deletesecuritycontext.htm
tech.root: secauthn
ms.assetid: 2a4dd697-ef90-4c37-ab74-0e5ab92794cd
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: DeleteSecurityContext, DeleteSecurityContext function [Security], _ssp_deletesecuritycontext, security.deletesecuritycontext, sspi/DeleteSecurityContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: sspi.h
req.include-header: Security.h
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
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - DeleteSecurityContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DeleteSecurityContext function


## -description


The <b>DeleteSecurityContext</b> function deletes the local data structures associated with the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> initiated by a previous call to the <a href="https://msdn.microsoft.com/21d965d4-3c03-4e29-a70d-4538c5c366b0">InitializeSecurityContext (General)</a> function or the <a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext (General)</a> function.


## -parameters




### -param phContext [in]

Handle of the security context to delete.


## -returns



If the function succeeds or the handle has already been deleted, the return value is <b>SEC_E_OK</b>.

If the function fails, the return value can be the following error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle passed to the function is not valid.

</td>
</tr>
</table>
 




## -remarks



The <b>DeleteSecurityContext</b> function terminates a security context and frees associated resources.

The caller must call this function for a security context when that security context is no longer needed. This is true if the security context is partial, incomplete, rejected, or failed. After the security context is successfully deleted, further use of that security context is not permitted and the handle is no longer valid.




## -see-also




<a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext (General)</a>



<a href="https://msdn.microsoft.com/21d965d4-3c03-4e29-a70d-4538c5c366b0">InitializeSecurityContext (General)</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374731(v=VS.85).aspx">SSPI Functions</a>
 

 

