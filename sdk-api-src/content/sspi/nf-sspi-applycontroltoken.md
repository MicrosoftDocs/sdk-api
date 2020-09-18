---
UID: NF:sspi.ApplyControlToken
title: ApplyControlToken function (sspi.h)
description: Provides a way to apply a control token to a security context.
helpviewer_keywords: ["ApplyControlToken","ApplyControlToken function [Security]","_ssp_applycontroltoken","security.applycontroltoken","sspi/ApplyControlToken"]
old-location: security\applycontroltoken.htm
tech.root: security
ms.assetid: 5ce13a05-874c-4e1a-9be8-aed98609791e
ms.date: 12/05/2018
ms.keywords: ApplyControlToken, ApplyControlToken function [Security], _ssp_applycontroltoken, security.applycontroltoken, sspi/ApplyControlToken
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
 - ApplyControlToken
 - sspi/ApplyControlToken
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
 - ApplyControlToken
---

# ApplyControlToken function


## -description

The <b>ApplyControlToken</b> function provides a way to apply a control token to a <a href="/windows/desktop/SecGloss/s-gly">security context</a>. A token can be received when the security context is being established by a call to 
the <a href="/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">InitializeSecurityContext (Schannel)</a> function or with a per-message security service, such as verify or unseal.

This function is supported only by the Schannel <a href="/windows/desktop/SecGloss/s-gly">security support provider</a> (SSP).

This function is not supported in kernel mode.

This function allows additional or replacement tokens to be applied to a context.

## -parameters

### -param phContext [in]

A handle to the context to which the token is applied.

For information about the way the Schannel SSP notifies the remote party of the shutdown, see the Remarks section of <a href="/windows/desktop/api/sspi/nf-sspi-decryptmessage">DecryptMessage (Schannel)</a>. For additional information on the use of this function, see 
<a href="/windows/desktop/SecAuthN/shutting-down-an-schannel-connection">Shutting Down an Schannel Connection</a>.

### -param pInput [in]

A pointer to a 
<a href="/windows/desktop/api/sspi/ns-sspi-secbufferdesc">SecBufferDesc</a> structure that contains a pointer to a 
<a href="/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a> structure that contains the input token to apply to the context.

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

The <b>ApplyControlToken</b> function can modify the context based on this token. Among the tokens that this function can add to the client context are <a href="/windows/desktop/api/schannel/ns-schannel-schannel_alert_token">SCHANNEL_ALERT_TOKEN</a> and <a href="/windows/desktop/api/schannel/ns-schannel-schannel_session_token">SCHANNEL_SESSION_TOKEN</a>.

This function can be used to shut down the <a href="/windows/desktop/SecGloss/s-gly">security context</a> that underlies an existing Schannel connection. For information about how to do this, see <a href="/windows/desktop/SecAuthN/shutting-down-an-schannel-connection">Shutting Down an Schannel Connection</a>.

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-decryptmessage">DecryptMessage (Schannel)</a>



<a href="/windows/desktop/api/sspi/nf-sspi-impersonatesecuritycontext">ImpersonateSecurityContext</a>



<a href="/windows/desktop/api/schannel/ns-schannel-schannel_alert_token">SCHANNEL_ALERT_TOKEN</a>



<a href="/windows/desktop/api/schannel/ns-schannel-schannel_session_token">SCHANNEL_SESSION_TOKEN</a>



<a href="/windows/desktop/SecAuthN/authentication-functions">SSPI Functions</a>



<a href="/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a>



<a href="/windows/desktop/api/sspi/ns-sspi-secbufferdesc">SecBufferDesc</a>