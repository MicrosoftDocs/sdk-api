---
UID: NS:d3d11.D3D11_AUTHENTICATED_QUERY_INPUT
title: D3D11_AUTHENTICATED_QUERY_INPUT
author: windows-sdk-content
description: Contains input data for the ID3D11VideoContext::QueryAuthenticatedChannel method.
old-location: mf\d3d11_authenticated_query_input.htm
tech.root: medfound
ms.assetid: D1FE4B31-A29D-4079-ABAE-8EB7DB0A0B42
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_ATTRIBUTES, D3D11_AUTHENTICATED_QUERY_CHANNEL_TYPE, D3D11_AUTHENTICATED_QUERY_CRYPTO_SESSION, D3D11_AUTHENTICATED_QUERY_CURRENT_ENCRYPTION_WHEN_ACCESSIBLE, D3D11_AUTHENTICATED_QUERY_DEVICE_HANDLE, D3D11_AUTHENTICATED_QUERY_ENCRYPTION_WHEN_ACCESSIBLE_GUID, D3D11_AUTHENTICATED_QUERY_ENCRYPTION_WHEN_ACCESSIBLE_GUID_COUNT, D3D11_AUTHENTICATED_QUERY_INPUT, D3D11_AUTHENTICATED_QUERY_INPUT structure [Media Foundation], D3D11_AUTHENTICATED_QUERY_OUTPUT_ID, D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_COUNT, D3D11_AUTHENTICATED_QUERY_PROTECTION, D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS, D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_COUNT, D3D11_AUTHENTICATED_QUERY_UNRESTRICTED_PROTECTED_SHARED_RESOURCE_COUNT, d3d11/D3D11_AUTHENTICATED_QUERY_INPUT, mf.d3d11_authenticated_query_input
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_AUTHENTICATED_QUERY_INPUT
product: Windows
targetos: Windows
req.typenames: D3D11_AUTHENTICATED_QUERY_INPUT
req.redist: 
---

# D3D11_AUTHENTICATED_QUERY_INPUT structure


## -description


Contains input data for the <a href="https://msdn.microsoft.com/4E059358-E1FD-4EDB-B1D4-982802385232">ID3D11VideoContext::QueryAuthenticatedChannel</a> method.




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

Output data structure: <a href="https://msdn.microsoft.com/1E2EBE2C-3749-47B5-B7A8-3EAE371981DB">D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_OUTPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_QUERY_CHANNEL_TYPE"></a><a id="d3d11_authenticated_query_channel_type"></a><dl>
<dt><b>D3D11_AUTHENTICATED_QUERY_CHANNEL_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Returns the type of authenticated channel.

Output data structure: <a href="https://msdn.microsoft.com/B71FAB00-76A6-40D0-97EA-7ECE99833A78">D3D11_AUTHENTICATED_QUERY_CHANNEL_TYPE_OUTPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_QUERY_CRYPTO_SESSION"></a><a id="d3d11_authenticated_query_crypto_session"></a><dl>
<dt><b>D3D11_AUTHENTICATED_QUERY_CRYPTO_SESSION</b></dt>
</dl>
</td>
<td width="60%">
Returns handles to the cryptographic session and Direct3D device that are associated with a specified decoder device.

Input data structure: <a href="https://msdn.microsoft.com/012E594C-4E0B-48A3-828A-A8F8B901F8E7">D3D11_AUTHENTICATED_QUERY_CRYPTO_SESSION_INPUT</a>


Output data structure: <a href="https://msdn.microsoft.com/8C52920A-25CC-4AD6-85E0-22D6A498D65A">D3D11_AUTHENTICATED_QUERY_CRYPTO_SESSION_OUTPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_QUERY_CURRENT_ENCRYPTION_WHEN_ACCESSIBLE"></a><a id="d3d11_authenticated_query_current_encryption_when_accessible"></a><dl>
<dt><b>D3D11_AUTHENTICATED_QUERY_CURRENT_ENCRYPTION_WHEN_ACCESSIBLE</b></dt>
</dl>
</td>
<td width="60%">
Returns the encryption type that is applied before content becomes accessible to the CPU or bus.

Output data structure: <a href="https://msdn.microsoft.com/C2958EC2-9D5B-471E-BB52-1F0001826C03">D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_ENCRYPTION_GUID_COUNT_OUTPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_QUERY_DEVICE_HANDLE"></a><a id="d3d11_authenticated_query_device_handle"></a><dl>
<dt><b>D3D11_AUTHENTICATED_QUERY_DEVICE_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
Returns a handle to the device that is associated with this authenticated channel.

Output data structure: <a href="https://msdn.microsoft.com/3553ACE5-FB28-4046-8E66-720A5447E05C">D3D11_AUTHENTICATED_QUERY_DEVICE_HANDLE_OUTPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_QUERY_ENCRYPTION_WHEN_ACCESSIBLE_GUID"></a><a id="d3d11_authenticated_query_encryption_when_accessible_guid"></a><dl>
<dt><b>D3D11_AUTHENTICATED_QUERY_ENCRYPTION_WHEN_ACCESSIBLE_GUID</b></dt>
</dl>
</td>
<td width="60%">
Returns one of the encryption types that can be used to encrypt content before it becomes accessible to the CPU or bus.

Input data structure: <a href="https://msdn.microsoft.com/359880E8-102C-4F99-ACD6-A1847A93BE25">D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_ENCRYPTION_GUID_INPUT</a>


Output data structure: <a href="https://msdn.microsoft.com/C782FABE-5B17-4C02-857C-AF2EE466903F">D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_ENCRYPTION_GUID_OUTPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_QUERY_ENCRYPTION_WHEN_ACCESSIBLE_GUID_COUNT"></a><a id="d3d11_authenticated_query_encryption_when_accessible_guid_count"></a><dl>
<dt><b>D3D11_AUTHENTICATED_QUERY_ENCRYPTION_WHEN_ACCESSIBLE_GUID_COUNT</b></dt>
</dl>
</td>
<td width="60%">
Returns the number of encryption types that can be used to encrypt content before it becomes accessible to the CPU or bus.

Output data structure: <a href="https://msdn.microsoft.com/C2958EC2-9D5B-471E-BB52-1F0001826C03">D3D11_AUTHENTICATED_QUERY_ACCESSIBILITY_ENCRYPTION_GUID_COUNT_OUTPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_QUERY_OUTPUT_ID"></a><a id="d3d11_authenticated_query_output_id"></a><dl>
<dt><b>D3D11_AUTHENTICATED_QUERY_OUTPUT_ID</b></dt>
</dl>
</td>
<td width="60%">
Returns one of the output identifiers that is associated with a specified cryptographic session and Direct3D device.

Input data structure: <a href="https://msdn.microsoft.com/2F4A6248-77DB-479B-B16C-81C3EE22937A">D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_INPUT</a>


Output data structure: <a href="https://msdn.microsoft.com/A7706E2B-B817-4D1C-B09D-D1803E0F8BFE">D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_OUTPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_COUNT"></a><a id="d3d11_authenticated_query_output_id_count"></a><dl>
<dt><b>D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_COUNT</b></dt>
</dl>
</td>
<td width="60%">
Returns the number of output identifiers that are associated with a specified cryptographic session and Direct3D device.

Input data structure: <a href="https://msdn.microsoft.com/9968985F-64F4-4BCC-801A-4929A52A10B7">D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_COUNT_INPUT</a>


Output data structure: <a href="https://msdn.microsoft.com/DDA18765-A086-40CE-8502-3A48B29DFCB6">D3D11_AUTHENTICATED_QUERY_OUTPUT_ID_COUNT_OUTPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_QUERY_PROTECTION"></a><a id="d3d11_authenticated_query_protection"></a><dl>
<dt><b>D3D11_AUTHENTICATED_QUERY_PROTECTION</b></dt>
</dl>
</td>
<td width="60%">
Returns the current protection level for the device.

Output data structure: <a href="https://msdn.microsoft.com/F70D5AFC-06A6-408D-A951-1280FBBF8E89">D3D11_AUTHENTICATED_QUERY_PROTECTION_OUTPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS"></a><a id="d3d11_authenticated_query_restricted_shared_resource_process"></a><dl>
<dt><b>D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS</b></dt>
</dl>
</td>
<td width="60%">
Returns information about a process that is allowed to open shared resources with restricted access.

Input data structure: <a href="https://msdn.microsoft.com/39B705E7-CCC0-48D3-A665-F42DE737FFAE">D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_INPUT</a>


Output data structure: <a href="https://msdn.microsoft.com/0668B546-6825-4AD9-85CF-CA238028B2E3">D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_OUTPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_COUNT"></a><a id="d3d11_authenticated_query_restricted_shared_resource_process_count"></a><dl>
<dt><b>D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_COUNT</b></dt>
</dl>
</td>
<td width="60%">
Returns the number of processes that are allowed to open shared resources with restricted access.

Output data structure: <a href="https://msdn.microsoft.com/E47F560D-DF50-40A5-AEB1-A594AB9C3B07">D3D11_AUTHENTICATED_QUERY_RESTRICTED_SHARED_RESOURCE_PROCESS_COUNT_OUTPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_QUERY_UNRESTRICTED_PROTECTED_SHARED_RESOURCE_COUNT"></a><a id="d3d11_authenticated_query_unrestricted_protected_shared_resource_count"></a><dl>
<dt><b>D3D11_AUTHENTICATED_QUERY_UNRESTRICTED_PROTECTED_SHARED_RESOURCE_COUNT</b></dt>
</dl>
</td>
<td width="60%">
Returns the number of protected shared resources that can be opened by any process with no restrictions.

Output data structure: <a href="https://msdn.microsoft.com/FE0ACC04-2FF2-43C2-8D65-5FFFF0C768CE">D3D11_AUTHENTICATED_QUERY_UNRESTRICTED_PROTECTED_SHARED_RESOURCE_COUNT_OUTPUT</a>


</td>
</tr>
</table>
 


### -field hChannel

A handle to the authenticated channel. To get the handle, call the <a href="https://msdn.microsoft.com/CA32D01B-B0B7-4F4F-8F48-747448DEC735">ID3D11AuthenticatedChannel::GetChannelHandle</a> method.


### -field SequenceNumber

The query sequence number. At the start of the session, generate a cryptographically secure 32-bit random number to use as the starting sequence number. For each query, increment the sequence number by 1.


## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>
 

 

