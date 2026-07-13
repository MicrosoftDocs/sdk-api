---
UID: NF:sspi.SaslInitializeSecurityContextA
title: SaslInitializeSecurityContextA function (sspi.h)
description: Wraps a standard call to the Security Support Provider Interface InitializeSecurityContext (General) function and processes SASL server cookies from the server. (ANSI)
helpviewer_keywords: ["ISC_REQ_CONFIDENTIALITY", "ISC_REQ_CONNECTION", "ISC_REQ_EXTENDED_ERROR", "ISC_REQ_INTEGRITY", "ISC_REQ_MUTUAL_AUTH", "ISC_REQ_REPLAY_DETECT", "ISC_REQ_SEQUENCE_DETECT", "ISC_REQ_STREAM", "SaslInitializeSecurityContextA", "sspi/SaslInitializeSecurityContextA"]
old-location: security\saslinitializesecuritycontext.htm
tech.root: security
ms.assetid: 9cc661b7-f1b0-4fb1-b799-5b318d87fd4d
ms.date: 12/05/2018
ms.keywords: ISC_REQ_CONFIDENTIALITY, ISC_REQ_CONNECTION, ISC_REQ_EXTENDED_ERROR, ISC_REQ_INTEGRITY, ISC_REQ_MUTUAL_AUTH, ISC_REQ_REPLAY_DETECT, ISC_REQ_SEQUENCE_DETECT, ISC_REQ_STREAM, SaslInitializeSecurityContext, SaslInitializeSecurityContext function [Security], SaslInitializeSecurityContextA, SaslInitializeSecurityContextW, security.saslinitializesecuritycontext, sspi/SaslInitializeSecurityContext, sspi/SaslInitializeSecurityContextA, sspi/SaslInitializeSecurityContextW
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SaslInitializeSecurityContextW (Unicode) and SaslInitializeSecurityContextA (ANSI)
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
 - SaslInitializeSecurityContextA
 - sspi/SaslInitializeSecurityContextA
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
 - SaslInitializeSecurityContext
 - SaslInitializeSecurityContextA
 - SaslInitializeSecurityContextW
---

# SaslInitializeSecurityContextA function


## -description

The <b>SaslInitializeSecurityContext</b> function wraps a standard call to the <a href="/windows/desktop/SecGloss/s-gly">Security Support Provider Interface</a> <a href="/windows/desktop/api/sspi/nf-sspi-initializesecuritycontexta">InitializeSecurityContext (General)</a> function and processes  SASL server cookies from the server.

## -parameters

### -param phCredential [in]

A handle to the <a href="/windows/desktop/SecGloss/c-gly">credentials</a> returned by the  
<a href="/windows/desktop/api/sspi/nf-sspi-acquirecredentialshandlea">AcquireCredentialsHandle</a> function used to build the <a href="/windows/desktop/SecGloss/s-gly">security context</a>. Using the <b>SaslInitializeSecurityContext</b> function requires at least OUTBOUND credentials.

### -param phContext [in]

Pointer to a <b>CtxtHandle</b> structure. On the first call to the <b>SaslInitializeSecurityContext</b> function, this pointer is <b>NULL</b>. On the second call, this parameter is a pointer to the handle to the partially formed context returned in the <i>phNewContext</i> parameter by the first call.

### -param pszTargetName [in]

Pointer to a Unicode or ANSI string that indicates the target of the context.

### -param fContextReq [in]

Bit flags that indicate the requirements of the context.  Flags used for this parameter are prefixed with ISC_REQ_; for example:  ISC_REQ_DELEGATE. Specify  combinations of the following attributes flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_REPLAY_DETECT"></a><a id="isc_req_replay_detect"></a><dl>
<dt><b>ISC_REQ_REPLAY_DETECT</b></dt>
</dl>
</td>
<td width="60%">
Detect replayed packets.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_SEQUENCE_DETECT"></a><a id="isc_req_sequence_detect"></a><dl>
<dt><b>ISC_REQ_SEQUENCE_DETECT</b></dt>
</dl>
</td>
<td width="60%">
Detect messages received out of sequence.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_CONFIDENTIALITY"></a><a id="isc_req_confidentiality"></a><dl>
<dt><b>ISC_REQ_CONFIDENTIALITY</b></dt>
</dl>
</td>
<td width="60%">
Encrypt messages.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_STREAM"></a><a id="isc_req_stream"></a><dl>
<dt><b>ISC_REQ_STREAM</b></dt>
</dl>
</td>
<td width="60%">
Support a stream-oriented connection.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_EXTENDED_ERROR"></a><a id="isc_req_extended_error"></a><dl>
<dt><b>ISC_REQ_EXTENDED_ERROR</b></dt>
</dl>
</td>
<td width="60%">
When errors occur, the remote party will be notified.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_CONNECTION"></a><a id="isc_req_connection"></a><dl>
<dt><b>ISC_REQ_CONNECTION</b></dt>
</dl>
</td>
<td width="60%">
The security context will not handle formatting messages.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_MUTUAL_AUTH"></a><a id="isc_req_mutual_auth"></a><dl>
<dt><b>ISC_REQ_MUTUAL_AUTH</b></dt>
</dl>
</td>
<td width="60%">
Client and server will be authenticated.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_INTEGRITY"></a><a id="isc_req_integrity"></a><dl>
<dt><b>ISC_REQ_INTEGRITY</b></dt>
</dl>
</td>
<td width="60%">
Sign messages and verify signatures.

</td>
</tr>
</table>
 

For  further descriptions of the various attributes, see 
<a href="/windows/desktop/SecAuthN/context-requirements">Context Requirements</a>.

### -param Reserved1 [in]

Reserved value; must be zero.

### -param TargetDataRep [in]

Indicates the data representation, such as byte ordering, on the target. Can be either SECURITY_NATIVE_DREP or SECURITY_NETWORK_DREP.

### -param pInput [in]

Pointer to a 
<a href="/windows/desktop/api/sspi/ns-sspi-secbufferdesc">SecBufferDesc</a> structure that contains pointers to the buffers supplied as input to the package. The pointer must be <b>NULL</b> on the first call to the function. On subsequent calls to the function, it is a pointer to a buffer allocated with enough memory to hold the token returned by the remote peer. 

SASL requires a single buffer of type <b>SECBUFFER_TOKEN</b> that contains the challenge received from the server.

### -param Reserved2 [in]

Reserved value; must be zero.

### -param phNewContext [out]

Pointer to a 
<a href="/windows/desktop/SecAuthN/sspi-handles">CtxtHandle</a> structure. On the first call to the <b>SaslInitializeSecurityContext</b> function, this pointer receives the new context handle. On the second call, <i>phNewContext</i> can be the same as the handle specified in the <i>phContext</i> parameter.

### -param pOutput [in, out]

Pointer to a 
<a href="/windows/desktop/api/sspi/ns-sspi-secbufferdesc">SecBufferDesc</a> structure that contains pointers to the 
<a href="/windows/desktop/api/sspi/ns-sspi-secbuffer">SecBuffer</a> structure that receives the output data. If a buffer was typed as SEC_READWRITE in the input, it will be there on output. The system will allocate a buffer for the security token if requested (through ISC_REQ_ALLOCATE_MEMORY) and fill in the address in the buffer descriptor for the security token.

### -param pfContextAttr [out]

Pointer to a variable to receive a set of bit flags that indicate the <a href="/windows/desktop/SecGloss/a-gly">attributes</a> of the established <a href="/windows/desktop/SecGloss/c-gly">context</a>. For a description of the various attributes, see 
<a href="/windows/desktop/SecAuthN/context-requirements">Context Requirements</a>. 

Flags used for this parameter are prefixed with ISC_RET_, such as ISC_RET_DELEGATE. 


 For a list of valid values, see the <i>fContextReq</i> parameter.

Do not check for security-related attributes until the final function call returns successfully. Attribute flags not related to security, such as the ASC_RET_ALLOCATED_MEMORY flag, can be checked before the final return.

<div class="alert"><b>Note</b>  Particular context attributes can change during a negotiation with a remote peer.</div>
<div> </div>

### -param ptsExpiry [out, optional]

Pointer to a <b>TimeStamp</b> structure that receives the expiration time of the context. It is recommended that the <a href="/windows/desktop/SecGloss/s-gly">security package</a> always return this value in local time. This parameter is optional and <b>NULL</b> should be passed for short-lived clients.

## -returns

If the call is completed successfully, this function returns SEC_E_OK. The following table shows some possible failure return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_ALGORITHM_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
Authz processing is not permitted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INSUFFICIENT_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory is available to complete the request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_TOKEN</b></dt>
</dl>
</td>
<td width="60%">
No Token buffer is located in the <i>pOutput</i> parameter, or the message failed to decrypt.

</td>
</tr>
</table>

## -remarks

> [!NOTE]
> The sspi.h header defines SaslInitializeSecurityContext as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
