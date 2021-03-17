---
UID: NS:d3d11.D3D11_AUTHENTICATED_CONFIGURE_OUTPUT
title: D3D11_AUTHENTICATED_CONFIGURE_OUTPUT (d3d11.h)
description: Contains the response from the ID3D11VideoContext::ConfigureAuthenticatedChannel method.
helpviewer_keywords: ["D3D11_AUTHENTICATED_CONFIGURE_OUTPUT","D3D11_AUTHENTICATED_CONFIGURE_OUTPUT structure [Media Foundation]","d3d11/D3D11_AUTHENTICATED_CONFIGURE_OUTPUT","mf.d3d11_authenticated_configure_output"]
old-location: mf\d3d11_authenticated_configure_output.htm
tech.root: mf
ms.assetid: 68DEC825-5D2E-4A78-B5DD-F7F697BB2980
ms.date: 12/05/2018
ms.keywords: D3D11_AUTHENTICATED_CONFIGURE_OUTPUT, D3D11_AUTHENTICATED_CONFIGURE_OUTPUT structure [Media Foundation], d3d11/D3D11_AUTHENTICATED_CONFIGURE_OUTPUT, mf.d3d11_authenticated_configure_output
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
req.typenames: D3D11_AUTHENTICATED_CONFIGURE_OUTPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_AUTHENTICATED_CONFIGURE_OUTPUT
 - d3d11/D3D11_AUTHENTICATED_CONFIGURE_OUTPUT
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
 - D3D11_AUTHENTICATED_CONFIGURE_OUTPUT
---

# D3D11_AUTHENTICATED_CONFIGURE_OUTPUT structure


## -description

Contains the response from the <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-configureauthenticatedchannel">ID3D11VideoContext::ConfigureAuthenticatedChannel</a> method.

## -struct-fields

### -field omac

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_omac">D3D11_OMAC</a> structure that contains a Message Authentication Code (MAC) of the data. The driver uses AES-based one-key CBC MAC (OMAC) to calculate this value for the block of data that appears after this structure member.

### -field ConfigureType

A GUID that specifies the command. For a list of GUIDs, see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_input">D3D11_AUTHENTICATED_CONFIGURE_INPUT</a>.

### -field hChannel

A handle to the authenticated channel.

### -field SequenceNumber

The command sequence number.

### -field ReturnCode

The result code for the command.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>