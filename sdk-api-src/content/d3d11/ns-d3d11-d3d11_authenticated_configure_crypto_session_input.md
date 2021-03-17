---
UID: NS:d3d11.D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT
title: D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT (d3d11.h)
description: Contains input data for a D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION command.
helpviewer_keywords: ["D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT","D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT structure [Media Foundation]","d3d11/D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT","mf.d3d11_authenticated_configure_crypto_session_input"]
old-location: mf\d3d11_authenticated_configure_crypto_session_input.htm
tech.root: mf
ms.assetid: 62DCE279-B0B6-4536-A14E-71F5B1BAA9ED
ms.date: 12/05/2018
ms.keywords: D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT, D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT structure [Media Foundation], d3d11/D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT, mf.d3d11_authenticated_configure_crypto_session_input
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
req.typenames: D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT
 - d3d11/D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT
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
 - D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT
---

# D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT structure


## -description

Contains input data for a <b>D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION</b> command.

## -struct-fields

### -field Parameters

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_authenticated_configure_input">D3D11_AUTHENTICATED_CONFIGURE_INPUT</a> structure that contains the command GUID and other data.

### -field DecoderHandle

A handle to the decoder device. Get this from <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodecoder-getdriverhandle">ID3D11VideoDecoder::GetDriverHandle</a>.

### -field CryptoSessionHandle

A handle to the cryptographic session. Get this from <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11cryptosession-getcryptosessionhandle">ID3D11CryptoSession::GetCryptoSessionHandle</a>.

### -field DeviceHandle

A handle to the Direct3D device. Get this from <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-queryauthenticatedchannel">D3D11VideoContext::QueryAuthenticatedChannel</a> using <b>D3D11_AUTHENTICATED_QUERY_DEVICE_HANDLE</b>.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>