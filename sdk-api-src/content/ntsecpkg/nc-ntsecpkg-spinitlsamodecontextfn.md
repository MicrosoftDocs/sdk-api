---
UID: NC:ntsecpkg.SpInitLsaModeContextFn
title: SpInitLsaModeContextFn
author: windows-driver-content
description: The client dispatch function used to establish a security context between a server and client.
old-location: security\spinitlsamodecontext.htm
old-project: SecAuthN
ms.assetid: e733d6fb-0ce6-4fd2-a8e2-54aa44602828
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: ISC_REQ_ALLOCATE_MEMORY, ISC_REQ_CONNECTION, ISC_REQ_DATAGRAM, ISC_REQ_DELEGATE, ISC_REQ_EXTENDED_ERROR, ISC_REQ_INTEGRITY, ISC_REQ_MUTUAL_AUTH, ISC_REQ_PROMPT_FOR_CREDS, ISC_REQ_REPLAY_DETECT, ISC_REQ_SEQUENCE_DETECT, ISC_REQ_STREAM, ISC_REQ_USE_DCE_STYLE, ISC_REQ_USE_SESSION_KEY, ISC_REQ_USE_SUPPLIED_CREDS, SpInitLsaModeContext, SpInitLsaModeContext function [Security], SpInitLsaModeContextFn, _ssp_spinitlsamodecontext, ntsecpkg/SpInitLsaModeContext, security.spinitlsamodecontext
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	SpInitLsaModeContext
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# SpInitLsaModeContextFn callback


## -description



			The <b>SpInitLsaModeContext</b> function is the client dispatch function used to establish a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">security context</a> between a server and client.

The <b>SpInitLsaModeContext</b> function is called when the client calls the 
<a href="https://msdn.microsoft.com/21d965d4-3c03-4e29-a70d-4538c5c366b0">InitializeSecurityContext (General)</a> function of the 
<a href="https://msdn.microsoft.com/91d2389b-1238-49d3-9fef-f1017a8072df">Security Support Provider Interface</a>.


## -parameters




### -param CredentialHandle [in]

Optional. Handle to the <a href="https://msdn.microsoft.com/library/windows/hardware/dn922689">credentials</a> to use for the context. <i>CredentialHandle</i> can be <b>NULL</b> if the <i>ContextHandle</i> parameter is not <b>NULL</b>.


### -param ContextHandle [in]

Optional. Handle to the context to use as the basis for this context. <i>ContextHandle</i> can be <b>NULL</b> if the <i>CredentialHandle</i> parameter is not <b>NULL</b>.


### -param TargetName [in]

Optional. Pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff564879">UNICODE_STRING</a> containing the name of the target of the context. The content of <i>TargetName</i> is package-specific and is not interpreted by the LSA.


### -param ContextRequirements [in]

Flags indicating the context attributes required by the client. The actual context attributes are returned in the <i>ContextAttributes</i> parameter. 




The following table lists the valid values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_DELEGATE"></a><a id="isc_req_delegate"></a><dl>
<dt><b>ISC_REQ_DELEGATE</b></dt>
</dl>
</td>
<td width="60%">
The server is allowed to impersonate the client.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_MUTUAL_AUTH"></a><a id="isc_req_mutual_auth"></a><dl>
<dt><b>ISC_REQ_MUTUAL_AUTH</b></dt>
</dl>
</td>
<td width="60%">
Both the client and the server are required to prove their identity.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_REPLAY_DETECT"></a><a id="isc_req_replay_detect"></a><dl>
<dt><b>ISC_REQ_REPLAY_DETECT</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> will support the detection of replayed packets.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_SEQUENCE_DETECT"></a><a id="isc_req_sequence_detect"></a><dl>
<dt><b>ISC_REQ_SEQUENCE_DETECT</b></dt>
</dl>
</td>
<td width="60%">
The security context will support the detection of out-of-order messages.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_USE_SESSION_KEY"></a><a id="isc_req_use_session_key"></a><dl>
<dt><b>ISC_REQ_USE_SESSION_KEY</b></dt>
</dl>
</td>
<td width="60%">
A new <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">session key</a> must be negotiated.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_PROMPT_FOR_CREDS"></a><a id="isc_req_prompt_for_creds"></a><dl>
<dt><b>ISC_REQ_PROMPT_FOR_CREDS</b></dt>
</dl>
</td>
<td width="60%">
If the client is an interactive user, the package must, if possible, prompt the user for the appropriate credentials.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_USE_SUPPLIED_CREDS"></a><a id="isc_req_use_supplied_creds"></a><dl>
<dt><b>ISC_REQ_USE_SUPPLIED_CREDS</b></dt>
</dl>
</td>
<td width="60%">
The input buffer contains package-specific credential information which should be used to authenticate the connection.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_ALLOCATE_MEMORY"></a><a id="isc_req_allocate_memory"></a><dl>
<dt><b>ISC_REQ_ALLOCATE_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The package must allocate memory. The caller must eventually call the 
<a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a> function to free memory allocated by the package.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_USE_DCE_STYLE"></a><a id="isc_req_use_dce_style"></a><dl>
<dt><b>ISC_REQ_USE_DCE_STYLE</b></dt>
</dl>
</td>
<td width="60%">
The caller expects a three-leg mutual authentication transaction.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_DATAGRAM"></a><a id="isc_req_datagram"></a><dl>
<dt><b>ISC_REQ_DATAGRAM</b></dt>
</dl>
</td>
<td width="60%">
A datagram-type communications channel should be used. For more information, see 
<a href="https://msdn.microsoft.com/f312796c-cbe6-4be9-9886-52fdb34ced6b">Datagram Contexts</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_CONNECTION"></a><a id="isc_req_connection"></a><dl>
<dt><b>ISC_REQ_CONNECTION</b></dt>
</dl>
</td>
<td width="60%">
A connection-type communications channel should be used. For more information see 
<a href="https://msdn.microsoft.com/82c6b1aa-304c-47f9-8e0f-ad70a89772aa">Connection-Oriented Contexts</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_EXTENDED_ERROR"></a><a id="isc_req_extended_error"></a><dl>
<dt><b>ISC_REQ_EXTENDED_ERROR</b></dt>
</dl>
</td>
<td width="60%">
If the context fails, generate an error reply message to send back to the client.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_STREAM"></a><a id="isc_req_stream"></a><dl>
<dt><b>ISC_REQ_STREAM</b></dt>
</dl>
</td>
<td width="60%">
A stream-type communications channel should be used. For more information, see 
<a href="https://msdn.microsoft.com/05a6b036-1f7f-473f-9813-a1e1534e0f0d">Stream Contexts</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_INTEGRITY"></a><a id="isc_req_integrity"></a><dl>
<dt><b>ISC_REQ_INTEGRITY</b></dt>
</dl>
</td>
<td width="60%">
Buffer integrity is verified; however, replayed and out-of-sequence messages will not be detected.

</td>
</tr>
</table>
 


### -param TargetDataRep [in]

Flag indicating the data representation, such as byte ordering, on the target. Contains SECURITY_NATIVE_DREP or SECURITY_NETWORK_DREP.


### -param InputBuffers [in]

Pointer to a 
<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a> structure containing the previous reply message from the server. The first time this function is called the <i>InputBuffers</i> parameter is <b>NULL</b>.


### -param NewContextHandle [out]

Pointer that receives a handle to the new <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>. When you have finished using the security context, release the handle by calling the <a href="https://msdn.microsoft.com/70e64bd3-7fdf-464b-bc0a-a0384a3e1a59">SpDeleteContext</a> function.


### -param OutputBuffers [out]

Pointer to a 
<a href="https://msdn.microsoft.com/fc6ef09c-3ba9-4bcb-a3c2-07422af8eaa9">SecBufferDesc</a> structure containing the security token to pass back to the server.


### -param ContextAttributes [out]

Pointer to flags specifying the attributes of the new context. The client requests a set of attributes using the <i>ContextRequirements</i> parameter. If the <i>ContextRequirements</i> flags do not match the <i>ContextAttributes</i> flags, the client must decide whether to continue or terminate. For a complete list of the valid flags, see 
<a href="https://msdn.microsoft.com/4a44b829-4202-46c0-b17e-04943fa067ab">Context Requirements</a>.


### -param ExpirationTime [out]

Pointer to a 
<a href="https://msdn.microsoft.com/0a609b32-dbd7-4905-8990-65ebabcd0668">TimeStamp</a> that receives the expiration time for the new context.


### -param MappedContext [out]

Pointer to a Boolean value. Set <i>MappedContext</i> to <b>TRUE</b> if the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> implements the user-mode SSP/AP functions.


### -param ContextData [out]

Pointer to a 
<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structure that receives the data to copy when creating a user-mode security context. Allocate memory for <i>ContextData</i> using the 
<a href="https://msdn.microsoft.com/cb87f1b1-3e1e-4add-8e74-ca7b4f8599ba">AllocateLsaHeap</a> function. The LSA will free the memory.


## -returns




						If the function succeeds and no more processing is required, return STATUS_SUCCESS. If processing is not complete, the function should return SEC_I_CONTINUE_NEEDED. When this value is returned, the caller must call the 
<a href="https://msdn.microsoft.com/21d965d4-3c03-4e29-a70d-4538c5c366b0">InitializeSecurityContext (General)</a> function again.
						

If the function fails to create the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> for any other reason, it should return an NTSTATUS code indicating the reason it failed.




## -remarks



The 
<a href="https://msdn.microsoft.com/bf443c15-0039-4ffa-a5ec-e8ef6a24dc80">SpAcceptLsaModeContext</a> function is the server-side function for creating a context.

SSP/APs must implement the <b>SpInitLsaModeContext</b> function; however, the actual name given to the implementation is up to the developer.

A pointer to the <b>SpInitLsaModeContext</b> function is available in the 
<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/cb87f1b1-3e1e-4add-8e74-ca7b4f8599ba">AllocateLsaHeap</a>



<a href="https://msdn.microsoft.com/21d965d4-3c03-4e29-a70d-4538c5c366b0">InitializeSecurityContext (General)</a>



<a href="https://msdn.microsoft.com/43ca0f9b-1393-48aa-9d9c-4dd19963a66d">SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/bf443c15-0039-4ffa-a5ec-e8ef6a24dc80">SpAcceptLsaModeContext</a>



<a href="https://msdn.microsoft.com/1ef3770b-197f-4d5b-9933-b7f6f63e5627">SpLsaModeInitialize</a>



<a href="https://msdn.microsoft.com/0a609b32-dbd7-4905-8990-65ebabcd0668">TimeStamp</a>
 

 

