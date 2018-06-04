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

# ID3D11VideoContext::GetDecoderBuffer


## -description


Gets a pointer to a decoder buffer.


## -parameters




### -param pDecoder [in]

A pointer to the <a href="https://msdn.microsoft.com/F25AFA0B-7413-40F0-AFF8-C9B4549305D2">ID3D11VideoDecoder</a> interface. To get this pointer, call <a href="https://msdn.microsoft.com/7EC2C7C3-F2EB-4357-BD53-308ABFFC9BE8">ID3D11VideoDevice::CreateVideoDecoder</a>.


### -param Type [in]

The type of buffer to retrieve, specified as a member of the <a href="https://msdn.microsoft.com/328B833F-750A-4A88-9571-EAB0532064BD">D3D11_VIDEO_DECODER_BUFFER_TYPE</a> enumeration.


### -param pBufferSize [out]

Receives the size of the buffer, in bytes.




### -param ppBuffer [out]

Receives a pointer to the start of the memory buffer.




## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The graphics driver allocates the buffers that are used for decoding. This method locks the Microsoft Direct3D
 surface that contains the buffer. When you are done using the buffer, call <a href="https://msdn.microsoft.com/C7BD4CA6-706D-4C3A-AED1-EDF1C65E41E0">ID3D11VideoContext::ReleaseDecoderBuffer</a> to unlock the surface.






## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

