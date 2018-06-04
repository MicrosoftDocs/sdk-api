---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

