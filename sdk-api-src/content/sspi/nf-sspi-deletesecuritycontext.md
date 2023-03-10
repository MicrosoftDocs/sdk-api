---
UID: NF:sspi.DeleteSecurityContext
title: DeleteSecurityContext function (sspi.h)
description: Deletes the local data structures associated with the specified security context initiated by a previous call to the InitializeSecurityContext (General) function or the AcceptSecurityContext (General) function.
helpviewer_keywords: ["DeleteSecurityContext","DeleteSecurityContext function [Security]","_ssp_deletesecuritycontext","security.deletesecuritycontext","sspi/DeleteSecurityContext"]
old-location: security\deletesecuritycontext.htm
tech.root: security
ms.assetid: 2a4dd697-ef90-4c37-ab74-0e5ab92794cd
ms.date: 12/05/2018
ms.keywords: DeleteSecurityContext, DeleteSecurityContext function [Security], _ssp_deletesecuritycontext, security.deletesecuritycontext, sspi/DeleteSecurityContext
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
 - DeleteSecurityContext
 - sspi/DeleteSecurityContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
 - schannel.dll
api_name:
 - DeleteSecurityContext
---

# DeleteSecurityContext function


## -description

The <b>DeleteSecurityContext</b> function deletes the local data structures associated with the specified <a href="/windows/desktop/SecGloss/s-gly">security context</a> initiated by a previous call to the <a href="/windows/desktop/api/sspi/nf-sspi-initializesecuritycontexta">InitializeSecurityContext (General)</a> function or the <a href="/windows/desktop/api/sspi/nf-sspi-acceptsecuritycontext">AcceptSecurityContext (General)</a> function.

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

<a href="/windows/desktop/api/sspi/nf-sspi-acceptsecuritycontext">AcceptSecurityContext (General)</a>



<a href="/windows/desktop/api/sspi/nf-sspi-initializesecuritycontexta">InitializeSecurityContext (General)</a>



<a href="/windows/desktop/SecAuthN/authentication-functions">SSPI Functions</a>