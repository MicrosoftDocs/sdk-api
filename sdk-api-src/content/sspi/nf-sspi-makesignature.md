---
UID: NF:sspi.MakeSignature
title: MakeSignature function (sspi.h)
description: Generates a cryptographic checksum of the message, and also includes sequencing information to prevent message loss or insertion.
helpviewer_keywords: ["0","1","2","3","4","MakeSignature","MakeSignature function [Security]","_ssp_makesignature","security.makesignature","sspi/MakeSignature"]
old-location: security\makesignature.htm
tech.root: security
ms.assetid: d17824b0-6121-48a3-b19b-d4fae3e1348e
ms.date: 12/05/2018
ms.keywords: 0, 1, 2, 3, 4, MakeSignature, MakeSignature function [Security], _ssp_makesignature, security.makesignature, sspi/MakeSignature
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
 - MakeSignature
 - sspi/MakeSignature
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
 - MakeSignature
---

# MakeSignature function


## -description

The <b>MakeSignature</b> function generates a cryptographic checksum of the message, and also includes sequencing information to prevent message loss or insertion. <b>MakeSignature</b> allows the application to choose between several cryptographic algorithms, if supported by the chosen mechanism. The <b>MakeSignature</b> function uses the <a href="/windows/desktop/SecGloss/s-gly">security context</a> referenced by the context handle.

This function is not supported by the Schannel <a href="/windows/desktop/SecGloss/s-gly">security support provider</a> (SSP).

## -parameters

### -param phContext [in]

A handle to the security context to use to sign the message.

### -param fQOP [in]

<a href="/windows/desktop/SecGloss/s-gly">Package</a>-specific flags that indicate the quality of protection. A security package can use this parameter to enable the selection of cryptographic algorithms.

When using the Digest SSP, this parameter must be set to zero.

### -param pMessage [in, out]

A pointer to a 
<a href="/windows/desktop/api/sspi/ns-sspi-secbufferdesc">SecBufferDesc</a> structure. On input, the structure references one or more 
<a href="/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a> structures that contain the message to be signed. The function does not process buffers with the SECBUFFER_READONLY_WITH_CHECKSUM  attribute.

The <a href="/windows/desktop/api/sspi/ns-sspi-secbufferdesc">SecBufferDesc</a> structure also references a <a href="/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a> structure of type SECBUFFER_TOKEN that receives the signature.

When the Digest SSP is used as an HTTP authentication protocol, the buffers should be configured as follows.

<table>
<tr>
<th>Buffer #/buffer type</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
<dt>SECBUFFER_TOKEN</dt>
</dl>
</td>
<td width="60%">
Empty.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
<dt>SECBUFFER_PKG_PARAMS</dt>
</dl>
</td>
<td width="60%">
Method.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
<dt>SECBUFFER_PKG_PARAMS</dt>
</dl>
</td>
<td width="60%">
URL.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
<dt>SECBUFFER_PKG_PARAMS</dt>
</dl>
</td>
<td width="60%">
HEntity. For more information, see 
<a href="/windows/desktop/SecAuthN/input-buffers-for-the-digest-challenge-response">Input Buffers for the Digest Challenge Response</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="4"></a><dl>
<dt><b>4</b></dt>
<dt>SECBUFFER_PADDING</dt>
</dl>
</td>
<td width="60%">
Empty. Receives the <a href="/windows/desktop/SecGloss/d-gly">signature</a>.

</td>
</tr>
</table>
 

When the Digest SSP is used as an SASL mechanism, the buffers should be configured as follows.

<table>
<tr>
<th>Buffer #/buffer type</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
<dt>SECBUFFER_TOKEN</dt>
</dl>
</td>
<td width="60%">
Empty. Receives the signature. This buffer must be large enough to hold the largest possible signature. Determine the size required by calling the 
<a href="/windows/desktop/api/sspi/nf-sspi-querycontextattributesa">QueryContextAttributes (General)</a> function and specifying SECPKG_ATTR_SIZES. Check the returned 
<a href="/windows/desktop/api/sspi/ns-sspi-secpkgcontext_sizes">SecPkgContext_Sizes</a> structure member <b>cbMaxSignature</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
<dt>SECBUFFER_DATA</dt>
</dl>
</td>
<td width="60%">
Message to be signed.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
<dt>SECBUFFER_PADDING</dt>
</dl>
</td>
<td width="60%">
Empty.

</td>
</tr>
</table>

### -param MessageSeqNo [in]

The sequence number that the transport application assigned to the message. If the transport application does not maintain sequence numbers, this parameter is zero.

When using the Digest SSP, this parameter must be set to zero. The Digest SSP manages sequence numbering internally.

## -returns

If the function succeeds, the function returns SEC_E_OK.

If the function fails, it returns one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_I_RENEGOTIATE</b></dt>
</dl>
</td>
<td width="60%">
The remote party requires a new handshake sequence or the application has just initiated a shutdown. Return to the negotiation loop and call 
<a href="/windows/desktop/api/sspi/nf-sspi-acceptsecuritycontext">AcceptSecurityContext (General)</a> or 
<a href="/windows/desktop/api/sspi/nf-sspi-initializesecuritycontexta">InitializeSecurityContext (General)</a> again. An empty input buffer is passed in the first call.

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
<i>pMessage</i> did not contain a valid SECBUFFER_TOKEN buffer or contained too few buffers.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_OUT_OF_SEQUENCE</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/SecGloss/n-gly">nonce</a> count is out of sequence.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_NO_AUTHENTICATING_AUTHORITY</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/SecGloss/s-gly">security context</a> (<i>phContext</i>) must be revalidated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The nonce count is not numeric.

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

The <b>MakeSignature</b> function generates a signature that is based on the message and the <a href="/windows/desktop/SecGloss/s-gly">session key</a> for the <a href="/windows/desktop/SecGloss/c-gly">context</a>.

The <a href="/windows/desktop/api/sspi/nf-sspi-verifysignature">VerifySignature</a> function verifies the messages signed by the <b>MakeSignature</b> function.

If the transport application created the security context to support sequence detection and the caller provides a sequence number, the function includes this information in the signature. This protects against reply, insertion, and suppression of messages. The <a href="/windows/desktop/SecGloss/s-gly">security package</a> incorporates the sequence number passed down from the transport application.

## -see-also

<a href="/windows/desktop/SecAuthN/authentication-functions">SSPI Functions</a>



<a href="/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a>



<a href="/windows/desktop/api/sspi/ns-sspi-secbufferdesc">SecBufferDesc</a>



<a href="/windows/desktop/api/sspi/nf-sspi-verifysignature">VerifySignature</a>