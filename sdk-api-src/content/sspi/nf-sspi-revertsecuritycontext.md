---
UID: NF:sspi.RevertSecurityContext
title: RevertSecurityContext function
author: windows-sdk-content
description: Allows a security package to discontinue the impersonation of the caller and restore its own security context.
old-location: security\revertsecuritycontext.htm
tech.root: secauthn
ms.assetid: d4ed1fe9-2e0a-4648-a010-1eae49ba03ee
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: RevertSecurityContext, RevertSecurityContext function [Security], _ssp_revertsecuritycontext, security.revertsecuritycontext, sspi/RevertSecurityContext
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
 - RevertSecurityContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RevertSecurityContext function


## -description


Allows a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> to discontinue the impersonation of the caller and restore its own <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>.


## -parameters




### -param phContext [in]

Handle of the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> being impersonated. This handle must have been obtained in the call to the 
<a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext (General)</a> function and used in the call to the 
<a href="https://msdn.microsoft.com/167eaf3b-b794-4587-946d-fa596f1f9411">ImpersonateSecurityContext</a> function.


## -returns



If the function succeeds, the return value is SEC_E_OK.

If the function fails, the return value can be one of the following error codes.

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



<b>RevertSecurityContext</b> is not available with all <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security packages</a> on all platforms. Typically, it is implemented only on platforms and with security packages for which a call to the 
<a href="https://msdn.microsoft.com/130ef0fe-bb13-4a65-b476-cd25ed234da1">QuerySecurityPackageInfo</a> function indicates impersonation support.




## -see-also




<a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext (General)</a>



<a href="https://msdn.microsoft.com/167eaf3b-b794-4587-946d-fa596f1f9411">ImpersonateSecurityContext</a>



<a href="authentication_functions.htm">SSPI Functions</a>
 

 

