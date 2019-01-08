---
UID: NF:sspi.InitializeSecurityContextW
title: InitializeSecurityContextW function
author: windows-sdk-content
description: Initiates the client side, outbound security context from a credential handle.
old-location: security\initializesecuritycontext__general_.htm
tech.root: SecAuthN
ms.assetid: 21d965d4-3c03-4e29-a70d-4538c5c366b0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Digest, ISC_REQ_ALLOCATE_MEMORY, ISC_REQ_CONFIDENTIALITY, ISC_REQ_CONNECTION, ISC_REQ_DELEGATE, ISC_REQ_EXTENDED_ERROR, ISC_REQ_HTTP, ISC_REQ_INTEGRITY, ISC_REQ_MANUAL_CRED_VALIDATION, ISC_REQ_MUTUAL_AUTH, ISC_REQ_NO_INTEGRITY, ISC_REQ_REPLAY_DETECT, ISC_REQ_SEQUENCE_DETECT, ISC_REQ_STREAM, ISC_REQ_USE_SESSION_KEY, ISC_REQ_USE_SUPPLIED_CREDS, InitializeSecurityContext, InitializeSecurityContext (General), InitializeSecurityContext function [Security], InitializeSecurityContextA, InitializeSecurityContextW, Kerberos or Negotiate, NTLM, Schannel/SSL, _ssp_initializesecuritycontext, security.initializesecuritycontext, security.initializesecuritycontext__general_, sspi/InitializeSecurityContext, sspi/InitializeSecurityContextA, sspi/InitializeSecurityContextW
ms.topic: function
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InitializeSecurityContextW (Unicode) and InitializeSecurityContextA (ANSI)
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
 - InitializeSecurityContext
 - InitializeSecurityContextA
 - InitializeSecurityContextW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# InitializeSecurityContextW function


## -description


The <b>InitializeSecurityContext (General)</b> function initiates the client side, outbound <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> from a credential handle. The function is used to build a security context between the client application and a remote peer. <b>InitializeSecurityContext (General)</b> returns a token that the client must pass to the remote peer, which the peer in turn submits to the local security implementation through the 
<a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext (General)</a> call. The token generated should be considered opaque by all callers.

Typically, the <b>InitializeSecurityContext (General)</b> function is called in a loop until a sufficient security context is established.

For information about using this function with a specific <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security support provider</a> (SSP), see the following topics.
<table>
<tr>
<th>Topic</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/f3d8c07b-db28-4f26-ba29-8733fc95bdb5">InitializeSecurityContext (CredSSP)</a>
</td>
<td>Initiates the client side, outbound security context from a credential handle by using the Credential Security Support Provider (CredSSP).</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/4b482dcc-3878-4bc6-85e4-229a1726cecc">InitializeSecurityContext (Digest)</a>
</td>
<td>Initiates the client side, outbound security context from a credential handle by using the Digest security package.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/b5c968dc-9343-44ed-acbc-a89c58c14e4a">InitializeSecurityContext (Kerberos)</a>
</td>
<td>Initiates the client side, outbound security context from a credential handle by using the Kerberos security package.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/031b0e82-f246-4291-aed3-f443ab152e00">InitializeSecurityContext (Negotiate)</a>
</td>
<td>Initiates the client side, outbound security context from a credential handle by using the Negotiate security package.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/a96b04f6-504c-4fd1-b62e-c08ba2b616e5">InitializeSecurityContext (NTLM)</a>
</td>
<td>Initiates the client side, outbound security context from a credential handle by using the NTLM security package.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/c451089a-d10d-469c-99dd-43d75a6b0b2a">InitializeSecurityContext (Schannel)</a>
</td>
<td>Initiates the client side, outbound security context from a credential handle by using the Schannel security package.</td>
</tr>
</table> 


## -parameters




### -param phCredential [in, optional]

A handle to the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">credentials</a> returned by 
<a href="https://msdn.microsoft.com/acda4cf3-39a6-4bd2-91a0-db1f191b57b5">AcquireCredentialsHandle (General)</a>. This handle is used to build the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>. The <b>InitializeSecurityContext (General)</b> function requires at least OUTBOUND credentials.


### -param phContext [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/94b622d0-7c04-4513-841f-0df9b5d49136">CtxtHandle</a> structure. On the first call to <b>InitializeSecurityContext (General)</b>, this pointer is <b>NULL</b>. On the second call, this parameter is a pointer to the handle to the partially formed context returned in the <i>phNewContext</i> parameter by the first call.

This parameter is optional with the Microsoft Digest SSP and can be set to <b>NULL</b>.

When using the Schannel SSP, on the first call to <b>InitializeSecurityContext (General)</b>, specify <b>NULL</b>. On future calls, specify the token received in the <i>phNewContext</i> parameter after the first call to this function.


#### - pTargetName [in, optional]

A pointer to a null-terminated string that indicates the target of the context. The string contents are <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security-package</a> specific, as described in the following table. This list is not exhaustive. Additional system SSPs and third party SSPs can be added to a system.

<table>
<tr>
<th>SSP in use</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="Digest"></a><a id="digest"></a><a id="DIGEST"></a><dl>
<dt><b>Digest</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Null-terminated string that uniquely identifies the URI of the requested resource. The string must be composed of characters that are allowed in a URI and must be representable by  the US ASCII code set.  Percent encoding can be used to represent characters outside the US ASCII code set.

</td>
</tr>
<tr>
<td width="40%"><a id="Kerberos_or_Negotiate"></a><a id="kerberos_or_negotiate"></a><a id="KERBEROS_OR_NEGOTIATE"></a><dl>
<dt><b>Kerberos or Negotiate</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Service principal name</a> (SPN) or the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> of the destination server.

</td>
</tr>
<tr>
<td width="40%"><a id="NTLM"></a><a id="ntlm"></a><dl>
<dt><b>NTLM</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
<a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">Service principal name</a> (SPN) or the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> of the destination server.

</td>
</tr>
<tr>
<td width="40%"><a id="Schannel_SSL"></a><a id="schannel_ssl"></a><a id="SCHANNEL_SSL"></a><dl>
<dt><b>Schannel/SSL</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Null-terminated string that uniquely identifies the target server. Schannel uses this value to verify the server certificate. Schannel also uses this value to locate the session in the session cache when reestablishing a connection. The cached session is used only if all of the following conditions are met:<ul>
<li>The target name is the same.</li>
<li>The cache entry has not expired.</li>
<li>The application process that calls the function is the same.</li>
<li>The logon session is the same.</li>
<li>The credential handle is the same.</li>
</ul>


</td>
</tr>
</table>
 


### -param fContextReq [in]

Bit flags that indicate requests for the context. Not all packages can support all requirements. Flags used for this parameter are prefixed with ISC_REQ_, for example,  ISC_REQ_DELEGATE. This parameter can be one or more of the following attributes flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_ALLOCATE_MEMORY"></a><a id="isc_req_allocate_memory"></a><dl>
<dt><b>ISC_REQ_ALLOCATE_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The security package allocates output buffers for you. When you have finished using the output buffers, free them by calling the  
<a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_CONFIDENTIALITY"></a><a id="isc_req_confidentiality"></a><dl>
<dt><b>ISC_REQ_CONFIDENTIALITY</b></dt>
</dl>
</td>
<td width="60%">
Encrypt messages by using the <a href="https://msdn.microsoft.com/2e09f262-9c3e-4db2-9285-017f5e1810c7">EncryptMessage</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_CONNECTION"></a><a id="isc_req_connection"></a><dl>
<dt><b>ISC_REQ_CONNECTION</b></dt>
</dl>
</td>
<td width="60%">
The security context will not handle formatting messages. This value is the default for the Kerberos, Negotiate, and NTLM security packages.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_DELEGATE"></a><a id="isc_req_delegate"></a><dl>
<dt><b>ISC_REQ_DELEGATE</b></dt>
</dl>
</td>
<td width="60%">
The server can use the context to authenticate to other servers as the client. The ISC_REQ_MUTUAL_AUTH flag must be set for this flag to work. Valid for Kerberos. Ignore this flag for <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">constrained delegation</a>.

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
<td width="40%"><a id="ISC_REQ_HTTP"></a><a id="isc_req_http"></a><dl>
<dt><b>ISC_REQ_HTTP</b></dt>
</dl>
</td>
<td width="60%">
Use Digest for HTTP. Omit this flag to use Digest as a SASL mechanism.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_INTEGRITY"></a><a id="isc_req_integrity"></a><dl>
<dt><b>ISC_REQ_INTEGRITY</b></dt>
</dl>
</td>
<td width="60%">
Sign messages and verify signatures by using the <a href="https://msdn.microsoft.com/2e09f262-9c3e-4db2-9285-017f5e1810c7">EncryptMessage</a> and <a href="https://msdn.microsoft.com/d17824b0-6121-48a3-b19b-d4fae3e1348e">MakeSignature</a> functions.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_MANUAL_CRED_VALIDATION"></a><a id="isc_req_manual_cred_validation"></a><dl>
<dt><b>ISC_REQ_MANUAL_CRED_VALIDATION</b></dt>
</dl>
</td>
<td width="60%">
Schannel must not authenticate the server automatically.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_MUTUAL_AUTH"></a><a id="isc_req_mutual_auth"></a><dl>
<dt><b>ISC_REQ_MUTUAL_AUTH</b></dt>
</dl>
</td>
<td width="60%">
The mutual authentication policy of the service will be satisfied.

<div class="alert"><b>Caution</b>  This does not necessarily mean that mutual authentication is performed, only that the authentication policy of the service is satisfied. To ensure that mutual authentication is performed, call the <a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a> function.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_NO_INTEGRITY"></a><a id="isc_req_no_integrity"></a><dl>
<dt><b>ISC_REQ_NO_INTEGRITY</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set, the <b>ISC_REQ_INTEGRITY</b> flag is ignored.

This value is supported only by the Negotiate and Kerberos <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security packages</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_REPLAY_DETECT"></a><a id="isc_req_replay_detect"></a><dl>
<dt><b>ISC_REQ_REPLAY_DETECT</b></dt>
</dl>
</td>
<td width="60%">
Detect replayed messages that have been encoded by using the <a href="https://msdn.microsoft.com/2e09f262-9c3e-4db2-9285-017f5e1810c7">EncryptMessage</a> or <a href="https://msdn.microsoft.com/d17824b0-6121-48a3-b19b-d4fae3e1348e">MakeSignature</a> functions.

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
<td width="40%"><a id="ISC_REQ_STREAM"></a><a id="isc_req_stream"></a><dl>
<dt><b>ISC_REQ_STREAM</b></dt>
</dl>
</td>
<td width="60%">
Support a stream-oriented connection.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_USE_SESSION_KEY"></a><a id="isc_req_use_session_key"></a><dl>
<dt><b>ISC_REQ_USE_SESSION_KEY</b></dt>
</dl>
</td>
<td width="60%">
A new <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">session key</a> must be negotiated.

This value is supported only by the Kerberos <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_USE_SUPPLIED_CREDS"></a><a id="isc_req_use_supplied_creds"></a><dl>
<dt><b>ISC_REQ_USE_SUPPLIED_CREDS</b></dt>
</dl>
</td>
<td width="60%">
Schannel must not attempt to supply credentials for the client automatically.

</td>
</tr>
</table>
 

The requested attributes may not be supported by the client. For more information, see the <i>pfContextAttr</i> parameter.

For  further descriptions of the various attributes, see 
<a href="https://msdn.microsoft.com/4a44b829-4202-46c0-b17e-04943fa067ab">Context Requirements</a>.


### -param Reserved1 [in]

This parameter is reserved and must be set to zero.


### -param TargetDataRep [in]

The data representation, such as byte ordering, on the target. This parameter can be either SECURITY_NATIVE_DREP or SECURITY_NETWORK_DREP.

This parameter is not used with Digest or Schannel. Set it to zero.


### -param pInput [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a> structure that contains pointers to the buffers supplied as input to the package. Unless the client context was initiated by the server, the value of this parameter must be <b>NULL</b> on the first call to the function. On subsequent calls to the function or when the client context was initiated by the server, the value of this parameter is a pointer to a buffer allocated with enough memory to hold the token returned by the remote computer.


### -param Reserved2 [in]

This parameter is reserved and must be set to zero.


### -param phNewContext [in, out, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/94b622d0-7c04-4513-841f-0df9b5d49136">CtxtHandle</a> structure. On the first call to <b>InitializeSecurityContext (General)</b>, this pointer receives the new context handle. On the second call, <i>phNewContext</i> can be the same as the handle specified in the <i>phContext</i> parameter.

When using the Schannel SSP,  on calls after the first call, pass the  handle returned here as the <i>phContext</i> parameter and specify <b>NULL</b> for <i>phNewContext</i>.


### -param pOutput [in, out, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a> structure that contains pointers to the 
<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structure that receives the output data. If a buffer was typed as SEC_READWRITE in the input, it will be there on output. The system will allocate a buffer for the security token if requested (through ISC_REQ_ALLOCATE_MEMORY) and fill in the address in the buffer descriptor for the security token.

When using the Microsoft Digest SSP,  this parameter receives the challenge response that must be sent to the server.

When using the Schannel SSP, if the ISC_REQ_ALLOCATE_MEMORY flag is specified, the Schannel SSP will allocate memory for  the buffer and put the appropriate information in the <a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a>. In addition, the caller must pass in a buffer of type <b>SECBUFFER_ALERT</b>. On output, if an alert is generated, this buffer  contains information about that alert, and the function fails.


### -param pfContextAttr [out]

A pointer to a variable to receive a set of bit flags that indicate the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attributes</a> of the established <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a>. For a description of the various attributes, see 
<a href="https://msdn.microsoft.com/4a44b829-4202-46c0-b17e-04943fa067ab">Context Requirements</a>. 

Flags used for this parameter are prefixed with ISC_RET, such as ISC_RET_DELEGATE. 


 For a list of valid values, see the <i>fContextReq</i> parameter.

Do not check for security-related attributes until the final function call returns successfully. Attribute flags that are not related to security, such as the ASC_RET_ALLOCATED_MEMORY flag, can be checked before the final return.

<div class="alert"><b>Note</b>  Particular context attributes can change during negotiation with a remote peer.</div>
<div> </div>

### -param ptsExpiry [out, optional]

A pointer to a <a href="https://msdn.microsoft.com/0a609b32-dbd7-4905-8990-65ebabcd0668">TimeStamp</a> structure that receives the expiration time of the context. It is recommended that the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> always return this value in local time. This parameter is optional and <b>NULL</b> should be passed for short-lived clients.

There is no expiration time for Microsoft Digest SSP security contexts or <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">credentials</a>.


## -returns



If the function succeeds, the function returns one of the following success codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_I_COMPLETE_AND_CONTINUE</b></dt>
</dl>
</td>
<td width="60%">
The client must call <a href="https://msdn.microsoft.com/a404d0a3-d1ea-4708-87d7-2d216e9a5f5f">CompleteAuthToken</a> and then pass the output to the server. The client then waits for a returned token and passes it, in another call, to <a href="https://msdn.microsoft.com/21d965d4-3c03-4e29-a70d-4538c5c366b0">InitializeSecurityContext (General)</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_I_COMPLETE_NEEDED</b></dt>
</dl>
</td>
<td width="60%">
The client must finish building the message and then call the 
<a href="https://msdn.microsoft.com/a404d0a3-d1ea-4708-87d7-2d216e9a5f5f">CompleteAuthToken</a> function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_I_CONTINUE_NEEDED</b></dt>
</dl>
</td>
<td width="60%">
The client must send the output token to the server and wait for a return token. The returned token is then passed in another call to <a href="https://msdn.microsoft.com/21d965d4-3c03-4e29-a70d-4538c5c366b0">InitializeSecurityContext (General)</a>. The output token can be empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_I_INCOMPLETE_CREDENTIALS</b></dt>
</dl>
</td>
<td width="60%">
Use with Schannel. The server has requested client authentication, and the supplied credentials either do not include a certificate or the certificate was not issued by a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> that is trusted by the server. For more information, see Remarks.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INCOMPLETE_MESSAGE</b></dt>
</dl>
</td>
<td width="60%">
Use with Schannel. Data for the whole message was not read from the wire.

When this value is returned, the <i>pInput</i> buffer contains a <a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structure with a <b>BufferType</b> member of <b>SECBUFFER_MISSING</b>. The <b>cbBuffer</b> member of <b>SecBuffer</b> contains a value that indicates the number of additional bytes that the function must read from the client before this function succeeds. While this number is not always accurate, using it can help improve performance by avoiding multiple calls to this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_OK</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> was successfully initialized. There is no need for another <a href="https://msdn.microsoft.com/21d965d4-3c03-4e29-a70d-4538c5c366b0">InitializeSecurityContext (General)</a> call. If the function returns an output token, that is, if the SECBUFFER_TOKEN in <i>pOutput</i> is of nonzero length, that token must be sent to the server.

</td>
</tr>
</table>
 

If the function fails, the function returns one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INSUFFICIENT_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory available to complete the requested action.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INTERNAL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred that did not map to an SSPI error code.

</td>
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
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INVALID_TOKEN</b></dt>
</dl>
</td>
<td width="60%">
The error is due to a malformed input token, such as a token corrupted in transit, a token of incorrect size, or a token passed into the wrong security package. Passing a token to the wrong package can happen if the client and server did not negotiate the proper security package.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_LOGON_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The logon failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_NO_AUTHENTICATING_AUTHORITY</b></dt>
</dl>
</td>
<td width="60%">
No authority could be contacted for authentication. The domain name of the authenticating party could be wrong, the domain could be unreachable, or there might have been a trust relationship failure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_NO_CREDENTIALS</b></dt>
</dl>
</td>
<td width="60%">
No credentials are available in the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_TARGET_UNKNOWN</b></dt>
</dl>
</td>
<td width="60%">
The target was not recognized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_UNSUPPORTED_FUNCTION</b></dt>
</dl>
</td>
<td width="60%">
A context attribute flag that is not valid (ISC_REQ_DELEGATE or ISC_REQ_PROMPT_FOR_CREDS) was specified in the <i>fContextReq</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_WRONG_PRINCIPAL</b></dt>
</dl>
</td>
<td width="60%">
The principal that received the authentication request is not the same as the one passed into the <i>pszTargetName</i> parameter. This indicates a failure in mutual authentication.

</td>
</tr>
</table>
 




## -remarks



The caller is responsible for determining whether the final context attributes are sufficient. If, for example, confidentiality was requested, but could not be established, some applications may choose to shut down the connection immediately.

If attributes of the security context are not sufficient, the client must free the partially created context by calling the 
<a href="https://msdn.microsoft.com/2a4dd697-ef90-4c37-ab74-0e5ab92794cd">DeleteSecurityContext</a> function.

The <b>InitializeSecurityContext (General)</b> function is used by a client to initialize an outbound context.

For a two-leg security context, the calling sequence is as follows:

<ol>
<li>The client calls the function with <i>phContext</i> set to <b>NULL</b> and fills in the buffer descriptor with the input message.</li>
<li>The security package examines the parameters and constructs an opaque token, placing it in the TOKEN element in the buffer array. If the <i>fContextReq</i> parameter includes the ISC_REQ_ALLOCATE_MEMORY flag, the security package allocates the memory and returns the pointer in the TOKEN element.</li>
<li>The client sends the token returned in the <i>pOutput</i> buffer to the target server. The server then passes the token as an input argument in a call to the <a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext (General)</a> function.</li>
<li>
<a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext (General)</a> may return a token, which the server sends to the client for a second call to <b>InitializeSecurityContext (General)</b> if the first call returned SEC_I_CONTINUE_NEEDED.</li>
</ol>
For multiple-leg security contexts, such as mutual authentication, the calling sequence is as follows:

<ol>
<li>The client calls the function as described earlier, but the package returns the SEC_I_CONTINUE_NEEDED success code.</li>
<li>The client sends the output token to the server and waits for the server's reply.</li>
<li>Upon receipt of the server's response, the client calls <b>InitializeSecurityContext (General)</b> again, with <i>phContext</i> set to the handle that was returned from the last call. The token received from the server is supplied in the <i>pInput</i> parameter.</li>
</ol>
If the server has successfully responded, the security package returns SEC_E_OK and a secure session is established.

If the function returns one of the error responses, the server's response is not accepted, and the session is not established.

If the function returns SEC_I_CONTINUE_NEEDED, SEC_I_COMPLETE_NEEDED, or SEC_I_COMPLETE_AND_CONTINUE, steps 2 and 3 are repeated.

To initialize a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>, more than one call to this function may be required, depending on the underlying authentication mechanism as well as the choices specified in the <i>fContextReq</i> parameter.

The <i>fContextReq</i> and <i>pfContextAttributes</i> parameters are bitmasks that represent various context attributes. For a description of the various attributes, see 
<a href="https://msdn.microsoft.com/4a44b829-4202-46c0-b17e-04943fa067ab">Context Requirements</a>. The <i>pfContextAttributes</i> parameter is valid on any successful return, but only on the final successful return should you examine the flags that pertain to security aspects of the context. Intermediate returns can set, for example, the ISC_RET_ALLOCATED_MEMORY flag.

If the ISC_REQ_USE_SUPPLIED_CREDS flag is set, the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> must look for a SECBUFFER_PKG_PARAMS buffer type in the <i>pInput</i> input buffer. This is not a generic solution, but it allows for a strong pairing of security package and application when appropriate.

If ISC_REQ_ALLOCATE_MEMORY was specified, the caller must free the memory by calling the 
<a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a> function.

For example, the input token could be the challenge from a LAN Manager. In this case, the output token would be the NTLM-encrypted response to the challenge.

The action the client takes depends on the return code from this function. If the return code is SEC_E_OK, there will be no second <b>InitializeSecurityContext (General)</b> call, and no response from the server is expected. If the return code is SEC_I_CONTINUE_NEEDED, the client expects a token in response from the server and passes it in a second call to <b>InitializeSecurityContext (General)</b>. The SEC_I_COMPLETE_NEEDED return code indicates that the client must finish building the message and call the <a href="https://msdn.microsoft.com/a404d0a3-d1ea-4708-87d7-2d216e9a5f5f">CompleteAuthToken</a> function. The SEC_I_COMPLETE_AND_CONTINUE code incorporates both of these actions.

If <b>InitializeSecurityContext (General)</b> returns success on the first (or only) call, then the caller must eventually call the <a href="https://msdn.microsoft.com/2a4dd697-ef90-4c37-ab74-0e5ab92794cd">DeleteSecurityContext</a> function on the returned handle, even if the call fails on a later leg of the authentication exchange.

The client may call <b>InitializeSecurityContext (General)</b> again after it has completed successfully. This indicates to the security package that a reauthentication is wanted.

Kernel mode callers have the following differences: the target name is a <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> string that must be allocated in virtual memory by using <a href="https://msdn.microsoft.com/a720dd89-c47c-4e48-bbc6-f2e02dfc4ed2">VirtualAlloc</a>; it must not be allocated from the pool. Buffers passed and supplied in <i>pInput</i> and <i>pOutput</i> must be in virtual memory, not in the pool.

When using the Schannel SSP, if the function returns SEC_I_INCOMPLETE_CREDENTIALS, check that you specified a valid and trusted certificate in your credentials. The certificate is specified when calling the <a href="https://msdn.microsoft.com/acda4cf3-39a6-4bd2-91a0-db1f191b57b5">AcquireCredentialsHandle (General)</a> function. The certificate must be a client authentication certificate issued by a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) trusted by the server. To obtain a list of the CAs trusted by the server, call the <a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a> function and specify the SECPKG_ATTR_ISSUER_LIST_EX attribute.

When using the Schannel SSP, after a client application receives an authentication certificate from a CA that is trusted by the server, the application  creates a new credential by calling the <a href="https://msdn.microsoft.com/acda4cf3-39a6-4bd2-91a0-db1f191b57b5">AcquireCredentialsHandle (General)</a> function and then calling <b>InitializeSecurityContext (General)</b> again, specifying the new credential in the <i>phCredential</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext (General)</a>



<a href="https://msdn.microsoft.com/acda4cf3-39a6-4bd2-91a0-db1f191b57b5">AcquireCredentialsHandle (General)</a>



<a href="https://msdn.microsoft.com/a404d0a3-d1ea-4708-87d7-2d216e9a5f5f">CompleteAuthToken</a>



<a href="https://msdn.microsoft.com/2a4dd697-ef90-4c37-ab74-0e5ab92794cd">DeleteSecurityContext</a>



<a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374731(v=VS.85).aspx">SSPI Functions</a>



<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a>



<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a>
 

 

