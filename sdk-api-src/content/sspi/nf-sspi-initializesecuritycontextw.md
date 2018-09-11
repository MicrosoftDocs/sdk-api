---
UID: NF:sspi.InitializeSecurityContextW
title: InitializeSecurityContextW function
author: windows-sdk-content
description: Initiates the client side, outbound security context from a credential handle.
old-location: security\initializesecuritycontext__credssp_.htm
tech.root: SecAuthN
ms.assetid: f3d8c07b-db28-4f26-ba29-8733fc95bdb5
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ISC_REQ_ALLOCATE_MEMORY, ISC_REQ_CONNECTION, ISC_REQ_DELEGATE, ISC_REQ_EXTENDED_ERROR, ISC_REQ_MANUAL_CRED_VALIDATION, ISC_REQ_MUTUAL_AUTH, ISC_REQ_SEQUENCE_DETECT, ISC_REQ_STREAM, ISC_REQ_USE_SUPPLIED_CREDS, InitializeSecurityContext, InitializeSecurityContext (CredSSP), InitializeSecurityContext function [Security], InitializeSecurityContextA, InitializeSecurityContextW, security.initializesecuritycontext__credssp_, sspi/InitializeSecurityContext, sspi/InitializeSecurityContextA, sspi/InitializeSecurityContextW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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


The <b>InitializeSecurityContext (CredSSP)</b> function initiates the client side, outbound  <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> from a credential handle. The function builds a security context between the client application and a remote peer. <b>InitializeSecurityContext (CredSSP)</b> returns a token that the client must pass to the remote peer; the peer in turn submits that token to the local security implementation through the 
<a href="https://msdn.microsoft.com/a53f733e-b646-4431-b021-a2c446308849">AcceptSecurityContext (CredSSP)</a> call. The token generated should be considered opaque by all callers.

Typically, the <b>InitializeSecurityContext (CredSSP)</b> function is called in a loop until a sufficient security context is established.


## -parameters




### -param phCredential [in, optional]

A handle to the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">credentials</a> returned by 
<a href="https://msdn.microsoft.com/3b73decf-75d4-4bc4-b7ca-5f16aaadff29">AcquireCredentialsHandle (CredSSP)</a>. This handle is used to build the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>. The <b>InitializeSecurityContext (CredSSP)</b> function requires at least OUTBOUND credentials.


### -param phContext [in, optional]

A pointer to a <a href="https://msdn.microsoft.com/94b622d0-7c04-4513-841f-0df9b5d49136">CtxtHandle</a> structure. On the first call to <b>InitializeSecurityContext (CredSSP)</b>, this pointer is <b>NULL</b>. On the second call, this parameter is a pointer to the handle to the partially formed context returned in the <i>phNewContext</i> parameter by the first call.

On the first call to <b>InitializeSecurityContext (CredSSP)</b>, specify <b>NULL</b>. On future calls, specify the token received in the <i>phNewContext</i> parameter after the first call to this function.


#### - pTargetName [in, optional]

A pointer to a null-terminated string that uniquely identifies the target server. Schannel uses this value to verify the server certificate. Schannel also uses this value to locate the session in the session cache when reestablishing a connection. The cached session is used only if all of the following conditions are met:

<ul>
<li>The target name is the same.</li>
<li>The cache entry has not expired.</li>
<li>The application process that calls the function is the same.</li>
<li>The logon session is the same.</li>
<li>The credential handle is the same.</li>
</ul>

### -param fContextReq [in]

Bit flags that indicate requests for the context. Not all packages can support all requirements. Flags used for this parameter are prefixed with ISC_REQ_, for example,  ISC_REQ_DELEGATE.

 This parameter can be one or more of the following attributes flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_ALLOCATE_MEMORY"></a><a id="isc_req_allocate_memory"></a><dl>
<dt><b>ISC_REQ_ALLOCATE_MEMORY</b></dt>
<dt>0x100</dt>
</dl>
</td>
<td width="60%">
The security package allocates output buffers for the caller. When you have finished using the output buffers, free them by calling the  
<a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_CONNECTION"></a><a id="isc_req_connection"></a><dl>
<dt><b>ISC_REQ_CONNECTION</b></dt>
<dt>0x800</dt>
</dl>
</td>
<td width="60%">
The security context will not handle formatting messages.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_EXTENDED_ERROR"></a><a id="isc_req_extended_error"></a><dl>
<dt><b>ISC_REQ_EXTENDED_ERROR</b></dt>
<dt>0x4000</dt>
</dl>
</td>
<td width="60%">
When errors occur, the remote party will be notified.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_MANUAL_CRED_VALIDATION"></a><a id="isc_req_manual_cred_validation"></a><dl>
<dt><b>ISC_REQ_MANUAL_CRED_VALIDATION</b></dt>
<dt>0x80000</dt>
</dl>
</td>
<td width="60%">
Credential Security Support Provider (CredSSP) must not authenticate the server automatically. This flag is always set when using CredSSP.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_SEQUENCE_DETECT"></a><a id="isc_req_sequence_detect"></a><dl>
<dt><b>ISC_REQ_SEQUENCE_DETECT</b></dt>
<dt>0x8</dt>
</dl>
</td>
<td width="60%">
Detect messages received out of sequence.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_STREAM"></a><a id="isc_req_stream"></a><dl>
<dt><b>ISC_REQ_STREAM</b></dt>
<dt>0x8000</dt>
</dl>
</td>
<td width="60%">
Support a stream-oriented connection.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_USE_SUPPLIED_CREDS"></a><a id="isc_req_use_supplied_creds"></a><dl>
<dt><b>ISC_REQ_USE_SUPPLIED_CREDS</b></dt>
<dt>0x80</dt>
</dl>
</td>
<td width="60%">
CredSSP must not attempt to supply credentials for the client automatically.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_DELEGATE"></a><a id="isc_req_delegate"></a><dl>
<dt><b>ISC_REQ_DELEGATE</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Indicates that the user's credentials are to be delegated to the server.

If this flag is not specified, an empty set of credentials is delegated to the server.

<b>Windows Server 2008 and Windows Vista:  </b>This flag is required.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_MUTUAL_AUTH"></a><a id="isc_req_mutual_auth"></a><dl>
<dt><b>ISC_REQ_MUTUAL_AUTH</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Indicates that server authentication is not required. Delegation policies are still enforced if this flag is  not specified.

<b>Windows Server 2008 and Windows Vista:  </b>This flag is ignored.

</td>
</tr>
</table>
 

The requested attributes may not be supported by the client. For more information, see the <i>pfContextAttr</i> parameter.

For  further descriptions of the various attributes, see 
<a href="https://msdn.microsoft.com/4a44b829-4202-46c0-b17e-04943fa067ab">Context Requirements</a>.


### -param Reserved1 [in]

Reserved. This parameter must be set to zero.


### -param TargetDataRep [in]

The data representation, such as byte ordering, on the target. This parameter can be either <b>SECURITY_NATIVE_DREP</b> or <b>SECURITY_NETWORK_DREP</b>.


### -param pInput [in, out, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a> structure that contains pointers to the buffers supplied as input to the package. Unless the client context was initiated by the server, the value of this parameter must be <b>NULL</b> on the first call to the function. On subsequent calls to the function or when the client context was initiated by the server, the value of this parameter is a pointer to a buffer allocated with enough memory to hold the token returned by the remote computer.

On calls to this function after the initial call, there must be two buffers. The first has type <b>SECBUFFER_TOKEN</b> and contains the token received from the server. The second buffer has type <b>SECBUFFER_EMPTY</b>; set both the <b>pvBuffer</b> and <b>cbBuffer</b> members to zero.


### -param Reserved2 [in]

Reserved. This parameter must be set to zero.


### -param phNewContext [in, out, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/94b622d0-7c04-4513-841f-0df9b5d49136">CtxtHandle</a> structure. On the first call to <b>InitializeSecurityContext (CredSSP)</b>, this pointer receives the new context handle. On the second call, <i>phNewContext</i> can be the same as the handle specified in the <i>phContext</i> parameter.

On calls after the first call, pass the  handle returned here as the <i>phContext</i> parameter and specify <b>NULL</b> for <i>phNewContext</i>.


### -param pOutput [out, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a> structure. This structure in turn contains pointers to the 
<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structure that receives the output data. If a buffer was typed as <b>SEC_READWRITE</b> in the input, it will be there on output. The system will allocate a buffer for the security token if requested (through <b>ISC_REQ_ALLOCATE_MEMORY</b>) and fill in the address in the buffer descriptor for the security token.

If the <b>ISC_REQ_ALLOCATE_MEMORY</b> flag is specified, CredSSP will allocate memory for  the buffer and put the appropriate information in the <a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a>.


### -param pfContextAttr [out]

A pointer to a set of bit flags that indicate the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attributes</a> of the established <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a>. For a description of the various attributes, see 
<a href="https://msdn.microsoft.com/4a44b829-4202-46c0-b17e-04943fa067ab">Context Requirements</a>.

Flags used for this parameter are prefixed with ISC_RET, such as <b>ISC_RET_DELEGATE</b>. 


 For a list of valid values, see the <i>fContextReq</i> parameter.

Do not check for security-related attributes until the final function call returns successfully. Attribute flags that are not related to security, such as the <b>ASC_RET_ALLOCATED_MEMORY</b> flag, can be checked before the final return.

<div class="alert"><b>Note</b>  Particular context attributes can change during negotiation with a remote peer.</div>
<div> </div>

### -param ptsExpiry [out, optional]

A pointer to a <a href="https://msdn.microsoft.com/0a609b32-dbd7-4905-8990-65ebabcd0668">TimeStamp</a> structure that receives the expiration time of the context. It is recommended that the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> always return this value in local time. This parameter is optional and <b>NULL</b> should be passed for short-lived clients.


## -returns



If the function succeeds, it returns one of the following success codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_INCOMPLETE_MESSAGE</b></dt>
</dl>
</td>
<td width="60%">
Data for the whole message was not read from the wire.

When this value is returned, the <i>pInput</i> buffer contains a <a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structure with a <b>BufferType</b> member of <b>SECBUFFER_MISSING</b>. The <b>cbBuffer</b> member of <b>SecBuffer</b> specifies the number of additional bytes that the function must read from the client before this function succeeds. While this number is not always accurate, using it can help improve performance by avoiding multiple calls to this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_OK</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> was successfully initialized. There is no need for another <a href="https://msdn.microsoft.com/f3d8c07b-db28-4f26-ba29-8733fc95bdb5">InitializeSecurityContext (CredSSP)</a> call. If the function returns an output token -- that is, if the <b>SECBUFFER_TOKEN</b> in <i>pOutput</i> is of nonzero length -- that token must be sent to the server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_I_COMPLETE_AND_CONTINUE</b></dt>
</dl>
</td>
<td width="60%">
The client must call <a href="https://msdn.microsoft.com/a404d0a3-d1ea-4708-87d7-2d216e9a5f5f">CompleteAuthToken</a> and then pass the output to the server. The client then waits for a returned token and passes it, in another call, to <a href="https://msdn.microsoft.com/f3d8c07b-db28-4f26-ba29-8733fc95bdb5">InitializeSecurityContext (CredSSP)</a>.

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
The client must send the output token to the server and wait for a return token. The client passes the returned token in another call to <a href="https://msdn.microsoft.com/f3d8c07b-db28-4f26-ba29-8733fc95bdb5">InitializeSecurityContext (CredSSP)</a>. The output token can be empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_I_INCOMPLETE_CREDENTIALS</b></dt>
</dl>
</td>
<td width="60%">
The server has requested client authentication, but either the supplied credentials do not include a certificate, or the certificate was not issued by a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> that the server  trusts. For more information, see Remarks.

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
The input token is malformed . Possible causes include a token corrupted in transit, a token of incorrect size, and a token passed into the wrong security package. This last condition can happen if the client and server did not negotiate the proper security package.

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
The value of the <i>fContextReq</i> parameter is not valid. Either a required flag was not specified, or a flag that is not supported by CredSSP was specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_WRONG_PRINCIPAL</b></dt>
</dl>
</td>
<td width="60%">
The principal that received the authentication request is not the same as the one passed into the <i>pszTargetName</i> parameter. This error indicates a failure in mutual authentication.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_DELEGATION_POLICY</b></dt>
</dl>
</td>
<td width="60%">
The policy does not support delegation of credentials to the target server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_POLICY_NLTM_ONLY</b></dt>
</dl>
</td>
<td width="60%">
Delegation of credentials to the target server is not allowed when mutual authentication is not achieved.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_MUTUAL_AUTH_FAILED</b></dt>
</dl>
</td>
<td width="60%">
Server authentication failed when the ISC_REQ_MUTUAL_AUTH flag is specified in the <i>fContextReq</i> parameter.

</td>
</tr>
</table>
 




## -remarks



The caller is responsible for determining whether the final context attributes are sufficient. If, for example, confidentiality was requested, but could not be established, some applications may choose to shut down the connection immediately.

If attributes of the security context are not sufficient, the client must free the partially created context by calling the 
<a href="https://msdn.microsoft.com/2a4dd697-ef90-4c37-ab74-0e5ab92794cd">DeleteSecurityContext</a> function.

The client calls the <b>InitializeSecurityContext (CredSSP)</b> function  to initialize an outbound context.

For a two-leg security context, the calling sequence is as follows:

<ol>
<li>The client calls the function with <i>phContext</i> set to <b>NULL</b> and fills in the buffer descriptor with the input message.</li>
<li>The security package examines the parameters and constructs an opaque token, placing it in the TOKEN element in the buffer array. If the <i>fContextReq</i> parameter includes the <b>ISC_REQ_ALLOCATE_MEMORY</b> flag, the security package allocates the memory and returns the pointer in the TOKEN element.</li>
<li>The client sends the token returned in the <i>pOutput</i> buffer to the target server. The server then passes the token as an input argument in a call to the <a href="https://msdn.microsoft.com/a53f733e-b646-4431-b021-a2c446308849">AcceptSecurityContext (CredSSP)</a> function.</li>
<li>
<a href="https://msdn.microsoft.com/a53f733e-b646-4431-b021-a2c446308849">AcceptSecurityContext (CredSSP)</a> may return a token. The server sends this token to the client through a second  <b>InitializeSecurityContext (CredSSP)</b> call if the first call returned <b>SEC_I_CONTINUE_NEEDED</b>.</li>
</ol>
If the server has successfully responded, the security package returns <b>SEC_E_OK</b> and a secure session is established.

If the function returns one of the error responses, the server's response is not accepted, and the session is not established.

If the function returns <b>SEC_I_CONTINUE_NEEDED</b>, <b>SEC_I_COMPLETE_NEEDED</b>, or <b>SEC_I_COMPLETE_AND_CONTINUE</b>, steps 2 and 3 are repeated.

Security-context initialization may require more than one call to this function, depending on the underlying authentication mechanism as well as the choices specified in the <i>fContextReq</i> parameter.

The <i>fContextReq</i> and <i>pfContextAttributes</i> parameters are bitmasks that represent various context attributes. For a description of the various attributes, see 
<a href="https://msdn.microsoft.com/4a44b829-4202-46c0-b17e-04943fa067ab">Context Requirements</a>. While the <i>pfContextAttributes</i> parameter is valid on any successful return, you should examine the flags that pertain to security aspects of the context only on the final successful return. Intermediate returns can set, for example, the <b>ISC_RET_ALLOCATED_MEMORY</b> flag.

If the <b>ISC_REQ_USE_SUPPLIED_CREDS</b> flag is set, the security package must look for a <b>SECBUFFER_PKG_PARAMS</b> buffer type in the <i>pInput</i> input buffer. While this is not a generic solution, it allows a strong pairing of security package and application when appropriate.

If <b>ISC_REQ_ALLOCATE_MEMORY</b> was specified, the caller must free the memory by calling the 
<a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a> function.

For example, the input token could be the challenge from a LAN Manager. In this case, the output token would be the NTLM-encrypted response to the challenge.

The action the client takes depends on the return code from this function. If the return code is <b>SEC_E_OK</b>, there will be no second <b>InitializeSecurityContext (CredSSP)</b> call, and no response from the server is expected. If the return code is <b>SEC_I_CONTINUE_NEEDED</b>, the client expects a token in response from the server and passes it in a second call to <b>InitializeSecurityContext (CredSSP)</b>. The <b>SEC_I_COMPLETE_NEEDED</b> return code indicates that the client must finish building the message and call the <a href="https://msdn.microsoft.com/a404d0a3-d1ea-4708-87d7-2d216e9a5f5f">CompleteAuthToken</a> function. The <b>SEC_I_COMPLETE_AND_CONTINUE</b> code incorporates both of these actions.

If <b>InitializeSecurityContext (CredSSP)</b> returns success on the first (or only) call, the caller must eventually call the <a href="https://msdn.microsoft.com/2a4dd697-ef90-4c37-ab74-0e5ab92794cd">DeleteSecurityContext</a> function on the returned handle, even if the call fails on a later leg of the authentication exchange.

The client may call <b>InitializeSecurityContext (CredSSP)</b> again after it has completed successfully. This indicates to the security package that a reauthentication is wanted.

Kernel-mode callers have the following differences: the target name is a <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> string that must be allocated in virtual memory by using <a href="https://msdn.microsoft.com/a720dd89-c47c-4e48-bbc6-f2e02dfc4ed2">VirtualAlloc</a>; it must not be allocated from the pool. Buffers passed and supplied in <i>pInput</i> and <i>pOutput</i> must be in virtual memory, not in the pool.

If the function returns <b>SEC_I_INCOMPLETE_CREDENTIALS</b>, check that the r credentials passed to the <a href="https://msdn.microsoft.com/3b73decf-75d4-4bc4-b7ca-5f16aaadff29">AcquireCredentialsHandle (CredSSP)</a> function specified a valid and trusted certificate The certificate must be a client authentication certificate issued by a certification authority trusted by the server. To obtain a list of the CAs trusted by the server, call the <a href="https://msdn.microsoft.com/4956c4ab-b71e-4960-b750-f3a79b87baac">QueryContextAttributes (CredSSP)</a> function with the <b>SECPKG_ATTR_ISSUER_LIST_EX</b> attribute.

After  receiving an authentication certificate from a certification authority that the server trusts, the client application  creates a new credential. It does so by calling the <a href="https://msdn.microsoft.com/3b73decf-75d4-4bc4-b7ca-5f16aaadff29">AcquireCredentialsHandle (CredSSP)</a> function and then calling <b>InitializeSecurityContext (CredSSP)</b> again, specifying the new credential in the <i>phCredential</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/a53f733e-b646-4431-b021-a2c446308849">AcceptSecurityContext (CredSSP)</a>



<a href="https://msdn.microsoft.com/3b73decf-75d4-4bc4-b7ca-5f16aaadff29">AcquireCredentialsHandle (CredSSP)</a>



<a href="https://msdn.microsoft.com/a404d0a3-d1ea-4708-87d7-2d216e9a5f5f">CompleteAuthToken</a>



<a href="https://msdn.microsoft.com/2a4dd697-ef90-4c37-ab74-0e5ab92794cd">DeleteSecurityContext</a>



<a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374731(v=VS.85).aspx">SSPI Functions</a>



<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a>



<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a>
 

 

