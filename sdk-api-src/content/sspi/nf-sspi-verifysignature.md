---
UID: NF:sspi.VerifySignature
title: VerifySignature function (sspi.h)
description: Verifies that a message signed by using the MakeSignature function was received in the correct sequence and has not been modified.
helpviewer_keywords: ["VerifySignature","VerifySignature function [Security]","_ssp_verifysignature","security.verifysignature","sspi/VerifySignature"]
old-location: security\verifysignature.htm
tech.root: security
ms.assetid: bebeef92-1d6e-4879-846f-12d706db0653
ms.date: 12/05/2018
ms.keywords: VerifySignature, VerifySignature function [Security], _ssp_verifysignature, security.verifysignature, sspi/VerifySignature
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
 - VerifySignature
 - sspi/VerifySignature
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
 - VerifySignature
---

# VerifySignature function


## -description

Verifies that a message signed by using the 
<a href="/windows/desktop/api/sspi/nf-sspi-makesignature">MakeSignature</a> function was received in the correct sequence and has not been modified.

## -parameters

### -param phContext [in]

A handle to the <a href="/windows/desktop/SecGloss/s-gly">security context</a> to use for the message.

### -param pMessage [in]

Pointer to a 
<a href="/windows/desktop/api/sspi/ns-sspi-secbufferdesc">SecBufferDesc</a> structure that references a set of 
<a href="/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a> structures that contain the message and signature to verify. The signature is in a <b>SecBuffer</b> structure of type SECBUFFER_TOKEN.

### -param MessageSeqNo [in]

Specifies the sequence number expected by the transport application, if any. If the transport application does not maintain sequence numbers, this parameter is zero.

### -param pfQOP [out]

Pointer to a <b>ULONG</b> variable that receives package-specific flags that indicate the quality of protection.

Some security packages ignore this parameter.

## -returns

If the function verifies that the message was received in the correct sequence and has not been modified, the return value is SEC_E_OK.

If the function determines that the message is not correct according to the information in the signature, the return value can be one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_OUT_OF_SEQUENCE</b></dt>
</dl>
</td>
<td width="60%">
The message was not received in the correct sequence.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_MESSAGE_ALTERED</b></dt>
</dl>
</td>
<td width="60%">
The message has been altered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The context handle specified by <i>phContext</i> is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_TOKEN</b></dt>
</dl>
</td>
<td width="60%">
<i>pMessage</i> did not contain a valid SECBUFFER_TOKEN buffer, or contained too few buffers.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_QOP_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The quality of protection negotiated between the client and server did not include <a href="/windows/desktop/SecGloss/i-gly">integrity</a> checking.

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Warning</b>  <p class="note">The <b>VerifySignature</b> function will fail if the message was signed using the <a href="/uwp/api/windows.security.cryptography.core.asymmetricalgorithmnames.rsasignpsssha512">RsaSignPssSha512</a> algorithm on a different version of Windows. For example, a message that was signed by calling the <a href="/windows/desktop/api/sspi/nf-sspi-makesignature">MakeSignature</a> function on Windows 8 will cause the <b>VerifySignature</b> function on Windows 8.1 to fail.

</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/sspi/nf-sspi-makesignature">MakeSignature</a>



<a href="/windows/desktop/SecAuthN/authentication-functions">SSPI Functions</a>



<a href="/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a>