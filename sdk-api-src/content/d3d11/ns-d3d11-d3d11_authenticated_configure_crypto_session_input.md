---
UID: NS:d3d11.D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT
title: D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT
author: windows-sdk-content
description: Contains input data for a D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION command.
old-location: mf\d3d11_authenticated_configure_crypto_session_input.htm
tech.root: medfound
ms.assetid: 62DCE279-B0B6-4536-A14E-71F5B1BAA9ED
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT, D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT structure [Media Foundation], d3d11/D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT, mf.d3d11_authenticated_configure_crypto_session_input
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
 - D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT
product: Windows
targetos: Windows
req.typenames: D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT
req.redist: 
---

# D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION_INPUT structure


## -description


Contains input data for a <b>D3D11_AUTHENTICATED_CONFIGURE_CRYPTO_SESSION</b> command.


## -struct-fields




### -field Parameters

A <a href="https://msdn.microsoft.com/11FC071E-9B73-4960-B675-A43DDF75AA0B">D3D11_AUTHENTICATED_CONFIGURE_INPUT</a> structure that contains the command GUID and other data.




### -field DecoderHandle

A handle to the decoder device. Get this from <a href="https://msdn.microsoft.com/CD9A46DB-C16D-4DF4-972B-2CE8398CEE98">ID3D11VideoDecoder::GetDriverHandle</a>.


### -field CryptoSessionHandle

A handle to the cryptographic session. Get this from <a href="https://msdn.microsoft.com/AEF55A0B-7052-4264-BC82-DACE06D20A81">ID3D11CryptoSession::GetCryptoSessionHandle</a>.


### -field DeviceHandle

A handle to the Direct3D device. Get this from <a href="https://msdn.microsoft.com/4E059358-E1FD-4EDB-B1D4-982802385232">D3D11VideoContext::QueryAuthenticatedChannel</a> using <b>D3D11_AUTHENTICATED_QUERY_DEVICE_HANDLE</b>.



## -see-also




<a href="https://msdn.microsoft.com/416159A4-F50E-4027-9367-727BA81D2A21">Direct3D 11 Video Structures</a>
 

 

