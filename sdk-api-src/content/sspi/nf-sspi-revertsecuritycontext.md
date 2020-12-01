---
UID: NF:sspi.RevertSecurityContext
title: RevertSecurityContext function (sspi.h)
description: Allows a security package to discontinue the impersonation of the caller and restore its own security context.
helpviewer_keywords: ["RevertSecurityContext","RevertSecurityContext function [Security]","_ssp_revertsecuritycontext","security.revertsecuritycontext","sspi/RevertSecurityContext"]
old-location: security\revertsecuritycontext.htm
tech.root: security
ms.assetid: d4ed1fe9-2e0a-4648-a010-1eae49ba03ee
ms.date: 12/05/2018
ms.keywords: RevertSecurityContext, RevertSecurityContext function [Security], _ssp_revertsecuritycontext, security.revertsecuritycontext, sspi/RevertSecurityContext
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RevertSecurityContext
 - sspi/RevertSecurityContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - RevertSecurityContext
---

# RevertSecurityContext function


## -description

Allows a <a href="/windows/desktop/SecGloss/s-gly">security package</a> to discontinue the impersonation of the caller and restore its own <a href="/windows/desktop/SecGloss/s-gly">security context</a>.

## -parameters

### -param phContext [in]

Handle of the <a href="/windows/desktop/SecGloss/s-gly">security context</a> being impersonated. This handle must have been obtained in the call to the 
<a href="/windows/desktop/api/sspi/nf-sspi-acceptsecuritycontext">AcceptSecurityContext (General)</a> function and used in the call to the 
<a href="/windows/desktop/api/sspi/nf-sspi-impersonatesecuritycontext">ImpersonateSecurityContext</a> function.

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

<b>RevertSecurityContext</b> is not available with all <a href="/windows/desktop/SecGloss/s-gly">security packages</a> on all platforms. Typically, it is implemented only on platforms and with security packages for which a call to the 
<a href="/windows/desktop/api/sspi/nf-sspi-querysecuritypackageinfoa">QuerySecurityPackageInfo</a> function indicates impersonation support.

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-acceptsecuritycontext">AcceptSecurityContext (General)</a>



<a href="/windows/desktop/api/sspi/nf-sspi-impersonatesecuritycontext">ImpersonateSecurityContext</a>



<a href="/windows/desktop/SecAuthN/authentication-functions">SSPI Functions</a>