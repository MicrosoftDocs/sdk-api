---
UID: NS:d3d11.D3D11_AUTHENTICATED_QUERY_INPUT
title: D3D11_AUTHENTICATED_QUERY_INPUT (d3d11.h)
description: Contains input data for the ID3D11VideoContext::QueryAuthenticatedChannel method.
helpviewer_keywords: ["D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_ATTRIBUTES","D3D11_AUTHENTICATED_QUERY_CHANNEL_TYPE","D3D11_AUTHENTICATED_QUERY_CRYPTO_SESSION","D3D11_AUTHENTICATED_QUERY_CURRENT_ENCRYPTION_WHEN_ACCESSIBLE","D3D11_AUTHENTICATED_QUERY_DEVICE_HANDLE","D3D11_AUTHENTICATED_QUERY_ENCRYPTION_WHEN_ACCESSIBLE_GUID","D3D11_AUTHENTICATED_QUERY_ENCRYPTION_WHEN_ACCESSIBLE_GUID_COUNT","D3D11_AUTHENTICATED_QUERY_INPUT","D3D11_AUTHENTICATED_QUERY_INPUT structure [Media Foundation]","D3D11_AUTHENTICATED_QUERY_OUTPUT_ID","D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_COUNT","D3D11_AUTHENTICATED_QUERY_PROTECTION","D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS","D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_COUNT","D3D11_AUTHENTICATED_QUERY_UNRESTRICTED_PROTECTED_SHARED_RESOURCE_COUNT","d3d11/D3D11_AUTHENTICATED_QUERY_INPUT","mf.d3d11_authenticated_query_input"]
old-location: mf\d3d11_authenticated_query_input.htm
tech.root: mf
ms.assetid: D1FE4B31-A29D-4079-ABAE-8EB7DB0A0B42
ms.date: 12/05/2018
ms.keywords: D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_ATTRIBUTES, D3D11_AUTHENTICATED_QUERY_CHANNEL_TYPE, D3D11_AUTHENTICATED_QUERY_CRYPTO_SESSION, D3D11_AUTHENTICATED_QUERY_CURRENT_ENCRYPTION_WHEN_ACCESSIBLE, D3D11_AUTHENTICATED_QUERY_DEVICE_HANDLE, D3D11_AUTHENTICATED_QUERY_ENCRYPTION_WHEN_ACCESSIBLE_GUID, D3D11_AUTHENTICATED_QUERY_ENCRYPTION_WHEN_ACCESSIBLE_GUID_COUNT, D3D11_AUTHENTICATED_QUERY_INPUT, D3D11_AUTHENTICATED_QUERY_INPUT structure [Media Foundation], D3D11_AUTHENTICATED_QUERY_OUTPUT_ID, D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_COUNT, D3D11_AUTHENTICATED_QUERY_PROTECTION, D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS, D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_COUNT, D3D11_AUTHENTICATED_QUERY_UNRESTRICTED_PROTECTED_SHARED_RESOURCE_COUNT, d3d11/D3D11_AUTHENTICATED_QUERY_INPUT, mf.d3d11_authenticated_query_input
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: D3D11_AUTHENTICATED_QUERY_INPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_AUTHENTICATED_QUERY_INPUT
 - d3d11/D3D11_AUTHENTICATED_QUERY_INPUT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_AUTHENTICATED_QUERY_INPUT
---

# D3D11_AUTHENTICATED_QUERY_INPUT structure


## -description

Contains input data for the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-queryauthenticatedchannel">ID3D11VideoContext::QueryAuthenticatedChannel</a> method.

## -struct-fields

### -field QueryType

A GUID that specifies the query. The following GUIDs are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_ATTRIBUTES"></a><a id="d3d11_authenticated_query_accessibility_attributes"></a><dl>
<dt><b>D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_ATTRIBUTES</b></dt>
</dl>
</td>
<td width="60%">
Returns the type of I/O bus that is used to send data to the GPU.

Output data structure: <a href="/windows/win32/api/d3d11/ns-d3d11-d3d11_authenticated_query_accessibility_output">D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_OUTPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_QUERY_CHANNEL_TYPE"></a><a id="d3d11_authenticated_query_channel_type"></a><dl>
<dt><b>D3D11_AUTHENTICATED_QUERY_CHANNEL_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Returns the type of authenticated channel.

Output data structure: <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_channel_type_output">D3D11_AUTHENTICATED_QUERY_CHANNEL_TYPE_OUTPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_QUERY_CRYPTO_SESSION"></a><a id="d3d11_authenticated_query_crypto_session"></a><dl>
<dt><b>D3D11_AUTHENTICATED_QUERY_CRYPTO_SESSION</b></dt>
</dl>
</td>
<td width="60%">
Returns handles to the cryptographic session and Direct3D device that are associated with a specified decoder device.

Input data structure: <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_crypto_session_input">D3D11_AUTHENTICATED_QUERY_CRYPTO_SESSION_INPUT</a>


Output data structure: <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_crypto_session_output">D3D11_AUTHENTICATED_QUERY_CRYPTO_SESSION_OUTPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_QUERY_CURRENT_ENCRYPTION_WHEN_ACCESSIBLE"></a><a id="d3d11_authenticated_query_current_encryption_when_accessible"></a><dl>
<dt><b>D3D11_AUTHENTICATED_QUERY_CURRENT_ENCRYPTION_WHEN_ACCESSIBLE</b></dt>
</dl>
</td>
<td width="60%">
Returns the encryption type that is applied before content becomes accessible to the CPU or bus.

Output data structure: <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_accessibility_encryption_guid_count_output">D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_ENCRYPTION_GUID_COUNT_OUTPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_QUERY_DEVICE_HANDLE"></a><a id="d3d11_authenticated_query_device_handle"></a><dl>
<dt><b>D3D11_AUTHENTICATED_QUERY_DEVICE_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
Returns a handle to the device that is associated with this authenticated channel.

Output data structure: <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_device_handle_output">D3D11_AUTHENTICATED_QUERY_DEVICE_HANDLE_OUTPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_QUERY_ENCRYPTION_WHEN_ACCESSIBLE_GUID"></a><a id="d3d11_authenticated_query_encryption_when_accessible_guid"></a><dl>
<dt><b>D3D11_AUTHENTICATED_QUERY_ENCRYPTION_WHEN_ACCESSIBLE_GUID</b></dt>
</dl>
</td>
<td width="60%">
Returns one of the encryption types that can be used to encrypt content before it becomes accessible to the CPU or bus.

Input data structure: <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_accessibility_encryption_guid_input">D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_ENCRYPTION_GUID_INPUT</a>


Output data structure: <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_accessibility_encryption_guid_output">D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_ENCRYPTION_GUID_OUTPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_QUERY_ENCRYPTION_WHEN_ACCESSIBLE_GUID_COUNT"></a><a id="d3d11_authenticated_query_encryption_when_accessible_guid_count"></a><dl>
<dt><b>D3D11_AUTHENTICATED_QUERY_ENCRYPTION_WHEN_ACCESSIBLE_GUID_COUNT</b></dt>
</dl>
</td>
<td width="60%">
Returns the number of encryption types that can be used to encrypt content before it becomes accessible to the CPU or bus.

Output data structure: <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_accessibility_encryption_guid_count_output">D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_ENCRYPTION_GUID_COUNT_OUTPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_QUERY_OUTPUT_ID"></a><a id="d3d11_authenticated_query_output_id"></a><dl>
<dt><b>D3D11_AUTHENTICATED_QUERY_OUTPUT_ID</b></dt>
</dl>
</td>
<td width="60%">
Returns one of the output identifiers that is associated with a specified cryptographic session and Direct3D device.

Input data structure: <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_output_id_input">D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_INPUT</a>


Output data structure: <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_output_id_output">D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_OUTPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_COUNT"></a><a id="d3d11_authenticated_query_output_id_count"></a><dl>
<dt><b>D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_COUNT</b></dt>
</dl>
</td>
<td width="60%">
Returns the number of output identifiers that are associated with a specified cryptographic session and Direct3D device.

Input data structure: <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_output_id_count_input">D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_COUNT_INPUT</a>


Output data structure: <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_output_id_count_output">D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_COUNT_OUTPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_QUERY_PROTECTION"></a><a id="d3d11_authenticated_query_protection"></a><dl>
<dt><b>D3D11_AUTHENTICATED_QUERY_PROTECTION</b></dt>
</dl>
</td>
<td width="60%">
Returns the current protection level for the device.

Output data structure: <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_protection_output">D3D11_AUTHENTICATED_QUERY_PROTECTION_OUTPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS"></a><a id="d3d11_authenticated_query_restricted_shared_resource_process"></a><dl>
<dt><b>D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS</b></dt>
</dl>
</td>
<td width="60%">
Returns information about a process that is allowed to open shared resources with restricted access.

Input data structure: <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_restricted_shared_resource_process_input">D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_INPUT</a>


Output data structure: <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_restricted_shared_resource_process_output">D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_OUTPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_COUNT"></a><a id="d3d11_authenticated_query_restricted_shared_resource_process_count"></a><dl>
<dt><b>D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_COUNT</b></dt>
</dl>
</td>
<td width="60%">
Returns the number of processes that are allowed to open shared resources with restricted access.

Output data structure: <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_restricted_shared_resource_process_count_output">D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_COUNT_OUTPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_QUERY_UNRESTRICTED_PROTECTED_SHARED_RESOURCE_COUNT"></a><a id="d3d11_authenticated_query_unrestricted_protected_shared_resource_count"></a><dl>
<dt><b>D3D11_AUTHENTICATED_QUERY_UNRESTRICTED_PROTECTED_SHARED_RESOURCE_COUNT</b></dt>
</dl>
</td>
<td width="60%">
Returns the number of protected shared resources that can be opened by any process with no restrictions.

Output data structure: <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_query_unrestricted_protected_shared_resource_count_output">D3D11_AUTHENTICATED_QUERY_UNRESTRICTED_PROTECTED_SHARED_RESOURCE_COUNT_OUTPUT</a>


</td>
</tr>
</table>

### -field hChannel

A handle to the authenticated channel. To get the handle, call the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11authenticatedchannel-getchannelhandle">ID3D11AuthenticatedChannel::GetChannelHandle</a> method.

### -field SequenceNumber

The query sequence number. At the start of the session, generate a cryptographically secure 32-bit random number to use as the starting sequence number. For each query, increment the sequence number by 1.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>