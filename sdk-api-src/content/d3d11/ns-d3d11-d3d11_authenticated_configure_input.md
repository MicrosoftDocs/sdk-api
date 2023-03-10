---
UID: NS:d3d11.D3D11_AUTHENTICATED_CONFIGURE_INPUT
title: D3D11_AUTHENTICATED_CONFIGURE_INPUT (d3d11.h)
description: Contains input data for the ID3D11VideoContext::ConfigureAuthenticatedChannel method.
helpviewer_keywords: ["D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION","D3D11_AUTHENTICATED_CONFIGURE_ENCRYPTION_WHEN_ACCESSIBLE","D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE","D3D11_AUTHENTICATED_CONFIGURE_INPUT","D3D11_AUTHENTICATED_CONFIGURE_INPUT structure [Media Foundation]","D3D11_AUTHENTICATED_CONFIGURE_PROTECTION","D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE","d3d11/D3D11_AUTHENTICATED_CONFIGURE_INPUT","mf.d3d11_authenticated_configure_input"]
old-location: mf\d3d11_authenticated_configure_input.htm
tech.root: mf
ms.assetid: 11FC071E-9B73-4960-B675-A43DDF75AA0B
ms.date: 12/05/2018
ms.keywords: D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION, D3D11_AUTHENTICATED_CONFIGURE_ENCRYPTION_WHEN_ACCESSIBLE, D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE, D3D11_AUTHENTICATED_CONFIGURE_INPUT, D3D11_AUTHENTICATED_CONFIGURE_INPUT structure [Media Foundation], D3D11_AUTHENTICATED_CONFIGURE_PROTECTION, D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE, d3d11/D3D11_AUTHENTICATED_CONFIGURE_INPUT, mf.d3d11_authenticated_configure_input
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
req.typenames: D3D11_AUTHENTICATED_CONFIGURE_INPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_AUTHENTICATED_CONFIGURE_INPUT
 - d3d11/D3D11_AUTHENTICATED_CONFIGURE_INPUT
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
 - D3D11_AUTHENTICATED_CONFIGURE_INPUT
---

# D3D11_AUTHENTICATED_CONFIGURE_INPUT structure


## -description

Contains input data for the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel">ID3D11VideoContext::ConfigureAuthenticatedChannel</a> method.

## -struct-fields

### -field omac

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_omac">D3D11_OMAC</a> structure that contains a Message Authentication Code (MAC) of the data. The driver uses AES-based one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.

### -field ConfigureType

A GUID that specifies the command. The following GUIDs are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION"></a><a id="d3d11_authenticated_configure_crypto_session"></a><dl>
<dt><b>D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION</b></dt>
</dl>
</td>
<td width="60%">
Associates a cryptographic session with a decoder device and a Direct3D device.



Input data: <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_crypto_session_input">D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_CONFIGURE_ENCRYPTION_WHEN_ACCESSIBLE"></a><a id="d3d11_authenticated_configure_encryption_when_accessible"></a><dl>
<dt><b>D3D11_AUTHENTICATED_CONFIGURE_ENCRYPTION_WHEN_ACCESSIBLE</b></dt>
</dl>
</td>
<td width="60%">
Sets the level of encryption that is performed before protected content becomes accessible to the CPU or bus.



Input data: <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_accessible_encryption_input">D3D11_AUTHENTICATED_CONFIGURE_ACCESSIBLE_ENCRYPTION_INPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE"></a><a id="d3d11_authenticated_configure_initialize"></a><dl>
<dt><b>D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE</b></dt>
</dl>
</td>
<td width="60%">
Initializes the authenticated channel.



Input data: <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_initialize_input">D3D11_AUTHENTICATED_CONFIGURE_INITIALIZE_INPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_CONFIGURE_PROTECTION"></a><a id="d3d11_authenticated_configure_protection"></a><dl>
<dt><b>D3D11_AUTHENTICATED_CONFIGURE_PROTECTION</b></dt>
</dl>
</td>
<td width="60%">
Enables or disables protection for the device.



Input data: <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_protection_input">D3D11_AUTHENTICATED_CONFIGURE_PROTECTION_INPUT</a>


</td>
</tr>
<tr>
<td width="40%"><a id="D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE"></a><a id="d3d11_authenticated_configure_shared_resource"></a><dl>
<dt><b>D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE</b></dt>
</dl>
</td>
<td width="60%">
Enables a process to open a shared resource, or disables a process from opening shared resources.



Input data: <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_shared_resource_input">D3D11_AUTHENTICATED_CONFIGURE_SHARED_RESOURCE_INPUT</a>


</td>
</tr>
</table>

### -field hChannel

A handle to the authenticated channel. To get the handle, call the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11authenticatedchannel-getchannelhandle">ID3D11AuthenticatedChannel::GetChannelHandle</a> method.

### -field SequenceNumber

The query sequence number. At the start of the session, generate a cryptographically secure 32-bit random number to use as the starting sequence number. For each query, increment the sequence number by 1.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>