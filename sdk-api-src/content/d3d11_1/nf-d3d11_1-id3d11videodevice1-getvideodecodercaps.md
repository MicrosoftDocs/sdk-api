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

# ID3D11VideoDevice1::GetVideoDecoderCaps


## -description


Retrieves capabilities and limitations of the video decoder.


## -parameters




### -param pDecoderProfile [in]

Type: <b>const GUID*</b>

The decode profile for which the capabilities are queried.


### -param SampleWidth [in]

Type: <b>UINT</b>

The video width for which the capabilities are queried.


### -param SampleHeight [in]

Type: <b>UINT</b>

The video height for which the capabilities are queried.


### -param pFrameRate [in]

Type: <b>const <a href="https://msdn.microsoft.com/0a878d11-dc90-4cad-bde5-54a135e53a86">DXGI_RATIONAL</a>*</b>

The frame rate of the video content. This information is used by the driver to determine whether the video can be decoded in real-time.


### -param BitRate [in]

Type: <b>UINT</b>

The bit rate of the video stream. A value of zero indicates that the bit rate can be ignored.


### -param pCryptoType [in]

Type: <b>const GUID*</b>

The type of cryptography used to encrypt the video stream. A value of NULL indicates that the video stream is not encrypted.


### -param pDecoderCaps [out]

Type: <b>UINT*</b>

A pointer to a bitwise OR combination of <a href="https://msdn.microsoft.com/8E3C86A4-5F73-4E6F-8F93-5564EA0BC113">D3D11_VIDEO_DECODER_CAPS</a> values specifying the decoder capabilities.




## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following error codes.

<table>
<tr>
<td>S_OK</td>
<td>The operation completed successfully.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid parameter was passed or this function was called using an invalid calling pattern.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/10E68945-6103-491D-8846-3B7C880FEAFD">ID3D11VideoDevice1</a>
 

 

