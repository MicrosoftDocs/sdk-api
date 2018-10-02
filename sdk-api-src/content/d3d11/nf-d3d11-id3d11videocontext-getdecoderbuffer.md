---
UID: NF:d3d11.ID3D11VideoContext.GetDecoderBuffer
title: ID3D11VideoContext::GetDecoderBuffer
author: windows-sdk-content
description: Gets a pointer to a decoder buffer.
old-location: mf\id3d11videocontext_getdecoderbuffer.htm
tech.root: MedFound
ms.assetid: 6842D5D7-6165-4428-91BD-2234BE5332B8
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetDecoderBuffer, GetDecoderBuffer method [Media Foundation], GetDecoderBuffer method [Media Foundation],ID3D11VideoContext interface, ID3D11VideoContext interface [Media Foundation],GetDecoderBuffer method, ID3D11VideoContext.GetDecoderBuffer, ID3D11VideoContext::GetDecoderBuffer, d3d11/ID3D11VideoContext::GetDecoderBuffer, mf.id3d11videocontext_getdecoderbuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoContext.GetDecoderBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



The graphics driver allocates the buffers that are used for decoding. This method locks the Microsoft Direct3Dsurface that contains the buffer. When you are done using the buffer, call <a href="https://msdn.microsoft.com/C7BD4CA6-706D-4C3A-AED1-EDF1C65E41E0">ID3D11VideoContext::ReleaseDecoderBuffer</a> to unlock the surface.






## -see-also




<a href="https://msdn.microsoft.com/6EF09C31-56C7-46B5-87AE-B1FE43EC66FC">ID3D11VideoContext</a>
 

 

