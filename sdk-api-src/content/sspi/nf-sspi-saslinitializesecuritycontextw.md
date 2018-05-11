---
UID: NF:sspi.SaslInitializeSecurityContextW
title: SaslInitializeSecurityContextW function
author: windows-driver-content
description: Wraps a standard call to the Security Support Provider Interface InitializeSecurityContext (General) function and processes SASL server cookies from the server.
old-location: security\saslinitializesecuritycontext.htm
old-project: SecAuthN
ms.assetid: 9cc661b7-f1b0-4fb1-b799-5b318d87fd4d
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ISC_REQ_CONFIDENTIALITY, ISC_REQ_CONNECTION, ISC_REQ_EXTENDED_ERROR, ISC_REQ_INTEGRITY, ISC_REQ_MUTUAL_AUTH, ISC_REQ_REPLAY_DETECT, ISC_REQ_SEQUENCE_DETECT, ISC_REQ_STREAM, SaslInitializeSecurityContext, SaslInitializeSecurityContext function [Security], SaslInitializeSecurityContextA, SaslInitializeSecurityContextW, security.saslinitializesecuritycontext, sspi/SaslInitializeSecurityContext, sspi/SaslInitializeSecurityContextA, sspi/SaslInitializeSecurityContextW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: SEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS, *PSEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Secur32.dll
api_name:
-	SaslInitializeSecurityContext
-	SaslInitializeSecurityContextA
-	SaslInitializeSecurityContextW
product: Windows
targetos: Windows
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# SaslInitializeSecurityContextW function


## -description


The <b>SaslInitializeSecurityContext</b> function wraps a standard call to the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Security Support Provider Interface</a> <a href="https://msdn.microsoft.com/21d965d4-3c03-4e29-a70d-4538c5c366b0">InitializeSecurityContext (General)</a> function and processes  SASL server cookies from the server.


## -parameters




### -param phCredential [in]

A handle to the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922689">credentials</a> returned by the  
<a href="https://msdn.microsoft.com/acda4cf3-39a6-4bd2-91a0-db1f191b57b5">AcquireCredentialsHandle</a> function used to build the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>. Using the <b>SaslInitializeSecurityContext</b> function requires at least OUTBOUND credentials.


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
<a href="https://msdn.microsoft.com/4a44b829-4202-46c0-b17e-04943fa067ab">Context Requirements</a>.


### -param Reserved1 [in]

Reserved value; must be zero.


### -param TargetDataRep [in]

Indicates the data representation, such as byte ordering, on the target. Can be either SECURITY_NATIVE_DREP or SECURITY_NETWORK_DREP.


### -param pInput [in]

Pointer to a 
<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a> structure that contains pointers to the buffers supplied as input to the package. The pointer must be <b>NULL</b> on the first call to the function. On subsequent calls to the function, it is a pointer to a buffer allocated with enough memory to hold the token returned by the remote peer. 

SASL requires a single buffer of type <b>SECBUFFER_TOKEN</b> that contains the challenge received from the server.


### -param Reserved2 [in]

Reserved value; must be zero.


### -param phNewContext [out]

Pointer to a 
<a href="https://msdn.microsoft.com/94b622d0-7c04-4513-841f-0df9b5d49136">CtxtHandle</a> structure. On the first call to the <b>SaslInitializeSecurityContext</b> function, this pointer receives the new context handle. On the second call, <i>phNewContext</i> can be the same as the handle specified in the <i>phContext</i> parameter.


### -param pOutput [in, out]

Pointer to a 
<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a> structure that contains pointers to the 
<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structure that receives the output data. If a buffer was typed as SEC_READWRITE in the input, it will be there on output. The system will allocate a buffer for the security token if requested (through ISC_REQ_ALLOCATE_MEMORY) and fill in the address in the buffer descriptor for the security token.


### -param pfContextAttr [out]

Pointer to a variable to receive a set of bit flags that indicate the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attributes</a> of the established <a href="https://msdn.microsoft.com/library/windows/hardware/hh439393">context</a>. For a description of the various attributes, see 
<a href="https://msdn.microsoft.com/4a44b829-4202-46c0-b17e-04943fa067ab">Context Requirements</a>. 

Flags used for this parameter are prefixed with ISC_RET_, such as ISC_RET_DELEGATE. 


 For a list of valid values, see the <i>fContextReq</i> parameter.

Do not check for security-related attributes until the final function call returns successfully. Attribute flags not related to security, such as the ASC_RET_ALLOCATED_MEMORY flag, can be checked before the final return.

<div class="alert"><b>Note</b>  Particular context attributes can change during a negotiation with a remote peer.</div>
<div> </div>

### -param ptsExpiry [out, optional]

Pointer to a <b>TimeStamp</b> structure that receives the expiration time of the context. It is recommended that the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> always return this value in local time. This parameter is optional and <b>NULL</b> should be passed for short-lived clients.


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
 



