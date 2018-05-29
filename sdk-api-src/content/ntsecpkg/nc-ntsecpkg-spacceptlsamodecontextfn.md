---
UID: NC:ntsecpkg.SpAcceptLsaModeContextFn
title: SpAcceptLsaModeContextFn
author: windows-sdk-content
description: Server dispatch function used to create a security context shared by a server and client.
old-location: security\spacceptlsamodecontext.htm
old-project: SecAuthN
ms.assetid: bf443c15-0039-4ffa-a5ec-e8ef6a24dc80
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ASC_REQ_ALLOCATE_MEMORY, ASC_REQ_CONNECTION, ASC_REQ_DATAGRAM, ASC_REQ_DELEGATE, ASC_REQ_EXTENDED_ERROR, ASC_REQ_INTEGRITY, ASC_REQ_MUTUAL_AUTH, ASC_REQ_PROMPT_FOR_CREDS, ASC_REQ_REPLAY_DETECT, ASC_REQ_SEQUENCE_DETECT, ASC_REQ_STREAM, ASC_REQ_USE_DCE_STYLE, ASC_REQ_USE_SESSION_KEY, ASC_REQ_USE_SUPPLIED_CREDS, SpAcceptLsaModeContext, SpAcceptLsaModeContext function [Security], SpAcceptLsaModeContextFn, _ssp_spacceptlsamodecontext, ntsecpkg/SpAcceptLsaModeContext, security.spacceptlsamodecontext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: ntsecpkg.h
req.include-header: 
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
req.typenames: TRUSTED_POSIX_OFFSET_INFO, *PTRUSTED_POSIX_OFFSET_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ntsecpkg.h
api_name:
-	SpAcceptLsaModeContext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# SpAcceptLsaModeContextFn callback function


## -description


Server dispatch function used to create a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> shared by a server and client.

The <b>SpAcceptLsaModeContext</b> function is called when the server calls the 
<a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext (General)</a> function of the 
<a href="https://msdn.microsoft.com/91d2389b-1238-49d3-9fef-f1017a8072df">Security Support Provider Interface</a>.


## -parameters




### -param CredentialHandle [in]

Optional. Handle to the credentials to use for the context.


### -param ContextHandle [in]

Optional. Handle to the current context.


### -param InputBuffer [in]

Pointer to a 
<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a> structure containing information from the client.


### -param ContextRequirements [in]

Flags indicating the context requirements. The following table lists the valid values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ASC_REQ_DELEGATE"></a><a id="asc_req_delegate"></a><dl>
<dt><b>ASC_REQ_DELEGATE</b></dt>
</dl>
</td>
<td width="60%">
The server is allowed to impersonate the client.

</td>
</tr>
<tr>
<td width="40%"><a id="ASC_REQ_MUTUAL_AUTH"></a><a id="asc_req_mutual_auth"></a><dl>
<dt><b>ASC_REQ_MUTUAL_AUTH</b></dt>
</dl>
</td>
<td width="60%">
Both the client and the server are required to prove their identity.

</td>
</tr>
<tr>
<td width="40%"><a id="ASC_REQ_REPLAY_DETECT"></a><a id="asc_req_replay_detect"></a><dl>
<dt><b>ASC_REQ_REPLAY_DETECT</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> will support the detection of replayed packets.

</td>
</tr>
<tr>
<td width="40%"><a id="ASC_REQ_SEQUENCE_DETECT"></a><a id="asc_req_sequence_detect"></a><dl>
<dt><b>ASC_REQ_SEQUENCE_DETECT</b></dt>
</dl>
</td>
<td width="60%">
The security context will support the detection of out-of-order messages.

</td>
</tr>
<tr>
<td width="40%"><a id="ASC_REQ_USE_SESSION_KEY"></a><a id="asc_req_use_session_key"></a><dl>
<dt><b>ASC_REQ_USE_SESSION_KEY</b></dt>
</dl>
</td>
<td width="60%">
A new <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">session key</a> must be negotiated.

</td>
</tr>
<tr>
<td width="40%"><a id="ASC_REQ_PROMPT_FOR_CREDS"></a><a id="asc_req_prompt_for_creds"></a><dl>
<dt><b>ASC_REQ_PROMPT_FOR_CREDS</b></dt>
</dl>
</td>
<td width="60%">
If the client is an interactive user, the package must, if possible, prompt the user for the appropriate credentials.

</td>
</tr>
<tr>
<td width="40%"><a id="ASC_REQ_USE_SUPPLIED_CREDS"></a><a id="asc_req_use_supplied_creds"></a><dl>
<dt><b>ASC_REQ_USE_SUPPLIED_CREDS</b></dt>
</dl>
</td>
<td width="60%">
The input buffer contains package-specific credential information which should be used to authenticate the connection.

</td>
</tr>
<tr>
<td width="40%"><a id="ASC_REQ_ALLOCATE_MEMORY"></a><a id="asc_req_allocate_memory"></a><dl>
<dt><b>ASC_REQ_ALLOCATE_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The package must allocate memory. The caller must eventually call the 
<a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a> function to free memory allocated by the security package.

</td>
</tr>
<tr>
<td width="40%"><a id="ASC_REQ_USE_DCE_STYLE"></a><a id="asc_req_use_dce_style"></a><dl>
<dt><b>ASC_REQ_USE_DCE_STYLE</b></dt>
</dl>
</td>
<td width="60%">
The caller expects a three-leg mutual authentication transaction.

</td>
</tr>
<tr>
<td width="40%"><a id="ASC_REQ_DATAGRAM"></a><a id="asc_req_datagram"></a><dl>
<dt><b>ASC_REQ_DATAGRAM</b></dt>
</dl>
</td>
<td width="60%">
A datagram-type communications channel should be used. For more information, see 
<a href="https://msdn.microsoft.com/f312796c-cbe6-4be9-9886-52fdb34ced6b">Datagram Contexts</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="ASC_REQ_CONNECTION"></a><a id="asc_req_connection"></a><dl>
<dt><b>ASC_REQ_CONNECTION</b></dt>
</dl>
</td>
<td width="60%">
A connection-type communications channel should be used. For more information see 
<a href="https://msdn.microsoft.com/82c6b1aa-304c-47f9-8e0f-ad70a89772aa">Connection-Oriented Contexts</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="ASC_REQ_EXTENDED_ERROR"></a><a id="asc_req_extended_error"></a><dl>
<dt><b>ASC_REQ_EXTENDED_ERROR</b></dt>
</dl>
</td>
<td width="60%">
If the context fails, generate an error reply message to send back to the client.

</td>
</tr>
<tr>
<td width="40%"><a id="ASC_REQ_STREAM"></a><a id="asc_req_stream"></a><dl>
<dt><b>ASC_REQ_STREAM</b></dt>
</dl>
</td>
<td width="60%">
A stream-type communications channel should be used. For more information, see 
<a href="https://msdn.microsoft.com/05a6b036-1f7f-473f-9813-a1e1534e0f0d">Stream Contexts</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="ASC_REQ_INTEGRITY"></a><a id="asc_req_integrity"></a><dl>
<dt><b>ASC_REQ_INTEGRITY</b></dt>
</dl>
</td>
<td width="60%">
Buffer integrity can be verified; however, replayed and out-of-sequence messages will not be detected.

</td>
</tr>
</table>
 


### -param TargetDataRep [in]

Flag indicating the data representation, such as byte ordering, to use. Contains SECURITY_NATIVE_DREP or SECURITY_NETWORK_DREP.


### -param NewContextHandle [out]

Pointer to an <b>LSA_SEC_HANDLE</b>. On the first call to 
<a href="https://msdn.microsoft.com/eaa15fed-4438-4e43-9be3-aa100ca453c7">AcceptSecurityContext</a>, this pointer receives the new context handle. On subsequent calls, <i>NewContextHandle</i> can be the same as the handle specified in the <i>ContextHandle</i> parameter.


### -param OutputBuffer [out]

Pointer to a 
<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a> structure that receives information to be sent to the client.


### -param ContextAttributes [out]

Pointer to flags specifying the context attributes that the server supports. For a list of valid values, see the <i>ContextRequirements</i> parameter.


### -param ExpirationTime [out]

Pointer to a 
<a href="https://msdn.microsoft.com/0a609b32-dbd7-4905-8990-65ebabcd0668">TimeStamp</a> that receives the expiration time for the context.


### -param MappedContext [out]

Pointer to a Boolean value. Set <i>MappedContext</i> to <b>TRUE</b> if the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> implements the user-mode SSP/AP functions.


### -param ContextData [out]

Optional. Pointer to a 
<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structure that receives context-specific data to copy when creating the user-mode <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>. Memory for <i>ContextData</i> must be allocated using the 
<a href="https://msdn.microsoft.com/cb87f1b1-3e1e-4add-8e74-ca7b4f8599ba">AllocateLsaHeap</a> function. The <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA) will free the memory.


## -returns




						If the <b>SpAcceptLsaModeContext</b> function succeeds and no more processing is required to establish the security context, return STATUS_SUCCESS. If additional processing is required, the function should return SEC_I_CONTINUE_NEEDED.

If the function fails to create the security context for any other reason, return an NTSTATUS code indicating the reason.




## -remarks




<a href="https://msdn.microsoft.com/e733d6fb-0ce6-4fd2-a8e2-54aa44602828">SpInitLsaModeContext</a> is the client-side function for creating a security context.

SSP/APs must implement the <b>SpAcceptLsaModeContext</b> function. The actual name given to the implementation is up to the developer.

A pointer to the <b>SpAcceptLsaModeContext</b> function is available in the 
<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/cb87f1b1-3e1e-4add-8e74-ca7b4f8599ba">AllocateLsaHeap</a>



<a href="https://msdn.microsoft.com/e733d6fb-0ce6-4fd2-a8e2-54aa44602828">SpInitLsaModeContext</a>



<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a>
 

 

