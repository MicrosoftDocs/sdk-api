---
UID: NC:ntsecpkg.SpExchangeMetaDataFn
title: SpExchangeMetaDataFn (ntsecpkg.h)
description: Sends metadata to a security support provider.
helpviewer_keywords: ["ISC_REQ_ALLOCATE_MEMORY","ISC_REQ_CONNECTION","ISC_REQ_DATAGRAM","ISC_REQ_DELEGATE","ISC_REQ_EXTENDED_ERROR","ISC_REQ_INTEGRITY","ISC_REQ_MUTUAL_AUTH","ISC_REQ_PROMPT_FOR_CREDS","ISC_REQ_REPLAY_DETECT","ISC_REQ_SEQUENCE_DETECT","ISC_REQ_STREAM","ISC_REQ_USE_DCE_STYLE","ISC_REQ_USE_SESSION_KEY","ISC_REQ_USE_SUPPLIED_CREDS","SpExchangeMetaDataFn","SpExchangeMetaDataFn callback","SpExchangeMetaDataFn callback function [Security]","ntsecpkg/SpExchangeMetaDataFn","security.spexchangemetadatafn"]
old-location: security\spexchangemetadatafn.htm
tech.root: security
ms.assetid: 35ef9276-1d61-44f3-912c-cf07dfcf7984
ms.date: 12/05/2018
ms.keywords: ISC_REQ_ALLOCATE_MEMORY, ISC_REQ_CONNECTION, ISC_REQ_DATAGRAM, ISC_REQ_DELEGATE, ISC_REQ_EXTENDED_ERROR, ISC_REQ_INTEGRITY, ISC_REQ_MUTUAL_AUTH, ISC_REQ_PROMPT_FOR_CREDS, ISC_REQ_REPLAY_DETECT, ISC_REQ_SEQUENCE_DETECT, ISC_REQ_STREAM, ISC_REQ_USE_DCE_STYLE, ISC_REQ_USE_SESSION_KEY, ISC_REQ_USE_SUPPLIED_CREDS, SpExchangeMetaDataFn, SpExchangeMetaDataFn callback, SpExchangeMetaDataFn callback function [Security], ntsecpkg/SpExchangeMetaDataFn, security.spexchangemetadatafn
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SpExchangeMetaDataFn
 - ntsecpkg/SpExchangeMetaDataFn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - SpExchangeMetaDataFn
---

# SpExchangeMetaDataFn callback function


## -description

Sends metadata to a <a href="/windows/desktop/SecGloss/s-gly">security support provider</a>. The metadata sent by this function is obtained by a previous call to the <a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-spquerymetadatafn">SpQueryMetaDataFn</a> function.

## -parameters

### -param CredentialHandle [in]

A handle to the <a href="/windows/desktop/SecGloss/c-gly">credentials</a> to use for the security context. If the <i>ContextHandle</i> parameter points to <b>NULL</b> on input, this function uses the value of this parameter to create a security context.

The value of this parameter  cannot be <b>NULL</b> if the <i>ContextHandle</i> parameter points to <b>NULL</b> on input.

### -param TargetName [in, optional]

A pointer to a 
<a href="/windows/desktop/api/subauth/ns-subauth-unicode_string">UNICODE_STRING</a> that contains the name of the target of the context.

### -param ContextRequirements [in]

Flags that indicate the context attributes required by the client. 




The following are valid values. Values can be combined by using a logical <b>OR</b> operation.

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
The <a href="/windows/desktop/SecGloss/s-gly">security context</a> will support the detection of replayed packets.

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
A new <a href="/windows/desktop/SecGloss/s-gly">session key</a> must be negotiated.

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
<a href="/windows/desktop/api/sspi/nf-sspi-freecontextbuffer">FreeContextBuffer</a> function to free memory allocated by the package.

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
<a href="/windows/desktop/SecAuthN/datagram-contexts">Datagram Contexts</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="ISC_REQ_CONNECTION"></a><a id="isc_req_connection"></a><dl>
<dt><b>ISC_REQ_CONNECTION</b></dt>
</dl>
</td>
<td width="60%">
A connection-type communications channel should be used. For more information see 
<a href="/windows/desktop/SecAuthN/connection-oriented-contexts">Connection-Oriented Contexts</a>.

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
<a href="/windows/desktop/SecAuthN/stream-contexts">Stream Contexts</a>.

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

### -param MetaDataLength [in]

The size, in characters, of the <i>MetaData</i> buffer.

### -param MetaData [in]

The metadata to send.

### -param ContextHandle [in, out]

A handle to the security handle to use. If this parameter points to <b>NULL</b> on input, this function allocates and initializes a security context by using the values of the <i>CredentialHandle</i> and <i>TargetName</i> parameters.

If this parameter points to <b>NULL</b> on input, the <i>CredentialHandle</i> cannot be <b>NULL</b>.

## -returns

If the function succeeds, return <b>STATUS_SUCCESS</b>, or an informational status code.

If the function fails, return an <b>NTSTATUS</b> error code that indicates the reason it failed. For more information, see Remarks.

## -remarks

A pointer to the <b>SpExchangeMetaDataFn</b> function is available in the 
<a href="/windows/desktop/api/ntsecpkg/ns-ntsecpkg-secpkg_function_table">SECPKG_FUNCTION_TABLE</a> structure received from the 
<a href="/windows/desktop/api/ntsecpkg/nc-ntsecpkg-splsamodeinitializefn">SpLsaModeInitialize</a> function.