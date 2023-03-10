---
UID: NF:sspi.FreeCredentialsHandle
title: FreeCredentialsHandle function (sspi.h)
description: Notifies the security system that the credentials are no longer needed.
helpviewer_keywords: ["FreeCredentialsHandle","FreeCredentialsHandle function [Security]","_ssp_freecredentialshandle","security.freecredentialshandle","sspi/FreeCredentialsHandle"]
old-location: security\freecredentialshandle.htm
tech.root: security
ms.assetid: e089618c-8233-475a-9725-39265c6427ab
ms.date: 12/05/2018
ms.keywords: FreeCredentialsHandle, FreeCredentialsHandle function [Security], _ssp_freecredentialshandle, security.freecredentialshandle, sspi/FreeCredentialsHandle
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
 - FreeCredentialsHandle
 - sspi/FreeCredentialsHandle
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
 - FreeCredentialsHandle
---

# FreeCredentialsHandle function


## -description

The <b>FreeCredentialsHandle</b> function notifies the security system that the <a href="/windows/desktop/SecGloss/c-gly">credentials</a> are no longer needed. An application calls this function to free the credential handle acquired in the call to the 
<a href="/windows/desktop/api/sspi/nf-sspi-acquirecredentialshandlea">AcquireCredentialsHandle (General)</a> function after calling the <a href="/windows/desktop/api/sspi/nf-sspi-deletesecuritycontext">DeleteSecurityContext</a> function to free any context handles associated with the credential. When all references to this credential set have been removed, the credentials themselves can be removed.

Failure to free credentials handles will result in memory leaks.

## -parameters

### -param phCredential [in]

A pointer to the <a href="/windows/desktop/SecAuthN/sspi-handles">CredHandle</a> handle obtained by using the 
<a href="/windows/desktop/api/sspi/nf-sspi-acquirecredentialshandlea">AcquireCredentialsHandle (General)</a> function.

## -returns

If the function succeeds, the function returns SEC_E_OK.

If the function fails, it returns the following error code.

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

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-acquirecredentialshandlea">AcquireCredentialsHandle (General)</a>



<a href="/windows/desktop/SecAuthN/authentication-functions">SSPI Functions</a>