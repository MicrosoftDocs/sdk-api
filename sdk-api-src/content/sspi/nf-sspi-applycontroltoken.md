---
UID: NF:sspi.ApplyControlToken
title: ApplyControlToken function
author: windows-sdk-content
description: Provides a way to apply a control token to a security context.
old-location: security\applycontroltoken.htm
tech.root: secauthn
ms.assetid: 5ce13a05-874c-4e1a-9be8-aed98609791e
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ApplyControlToken, ApplyControlToken function [Security], _ssp_applycontroltoken, security.applycontroltoken, sspi/ApplyControlToken
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
 - ApplyControlToken
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ApplyControlToken function


## -description


The <b>ApplyControlToken</b> function provides a way to apply a control token to a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>. A token can be received when the security context is being established by a call to 
the <a href="https://msdn.microsoft.com/c451089a-d10d-469c-99dd-43d75a6b0b2a">InitializeSecurityContext (Schannel)</a> function or with a per-message security service, such as verify or unseal.

This function is supported only by the Schannel <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security support provider</a> (SSP).

This function is not supported in kernel mode.

This function allows additional or replacement tokens to be applied to a context.


## -parameters




### -param phContext [in]

A handle to the context to which the token is applied.

For information about the way the Schannel SSP notifies the remote party of the shutdown, see the Remarks section of <a href="https://msdn.microsoft.com/5d7c8598-2d6b-4839-ae98-dff964bc962c">DecryptMessage (Schannel)</a>. For additional information on the use of this function, see 
<a href="https://msdn.microsoft.com/7081ba1f-df3c-41b4-96da-24d44e74d714">Shutting Down an Schannel Connection</a>.


### -param pInput [in]

A pointer to a 
<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a> structure that contains a pointer to a 
<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structure that contains the input token to apply to the context.


## -returns



If the function succeeds, the function returns SEC_E_OK.

If the function fails, it returns a nonzero error code. The following error code is one of the possible error codes that can be returned.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_UNSUPPORTED_FUNCTION</b></dt>
</dl>
</td>
<td width="60%">
This value is returned by Schannel kernel mode to indicate that this function is not supported.

</td>
</tr>
</table>
 




## -remarks



The <b>ApplyControlToken</b> function can modify the context based on this token. Among the tokens that this function can add to the client context are <a href="https://msdn.microsoft.com/1c3a896d-4252-44ef-9e4b-6ad00e3d6f05">SCHANNEL_ALERT_TOKEN</a> and <a href="https://msdn.microsoft.com/3c8f5380-eead-4495-8dff-a9561a787930">SCHANNEL_SESSION_TOKEN</a>.

This function can be used to shut down the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> that underlies an existing Schannel connection. For information about how to do this, see <a href="https://msdn.microsoft.com/7081ba1f-df3c-41b4-96da-24d44e74d714">Shutting Down an Schannel Connection</a>.




## -see-also




<a href="https://msdn.microsoft.com/5d7c8598-2d6b-4839-ae98-dff964bc962c">DecryptMessage (Schannel)</a>



<a href="https://msdn.microsoft.com/167eaf3b-b794-4587-946d-fa596f1f9411">ImpersonateSecurityContext</a>



<a href="https://msdn.microsoft.com/1c3a896d-4252-44ef-9e4b-6ad00e3d6f05">SCHANNEL_ALERT_TOKEN</a>



<a href="https://msdn.microsoft.com/3c8f5380-eead-4495-8dff-a9561a787930">SCHANNEL_SESSION_TOKEN</a>



<a href="authentication_functions.htm">SSPI Functions</a>



<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a>



<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a>
 

 

