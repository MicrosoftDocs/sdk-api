---
UID: NF:d3d11.ID3D11VideoDevice.CreateVideoDecoder
title: ID3D11VideoDevice::CreateVideoDecoder
author: windows-sdk-content
description: Creates a video decoder device for Microsoft Direct3D 11.
old-location: mf\id3d11videodevice_createvideodecoder.htm
tech.root: medfound
ms.assetid: 7EC2C7C3-F2EB-4357-BD53-308ABFFC9BE8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateVideoDecoder, CreateVideoDecoder method [Media Foundation], CreateVideoDecoder method [Media Foundation],ID3D11VideoDevice interface, ID3D11VideoDevice interface [Media Foundation],CreateVideoDecoder method, ID3D11VideoDevice.CreateVideoDecoder, ID3D11VideoDevice::CreateVideoDecoder, d3d11/ID3D11VideoDevice::CreateVideoDecoder, mf.id3d11videodevice_createvideodecoder
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
 - ID3D11VideoDevice.CreateVideoDecoder
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11VideoDevice::CreateVideoDecoder


## -description


Creates a video decoder device for Microsoft Direct3D 11.


## -parameters




### -param pVideoDesc [in]

A pointer to a <a href="https://msdn.microsoft.com/668D994C-B875-4666-B940-1052A6DE6AA1">D3D11_VIDEO_DECODER_DESC</a> structure that describes the video stream and the decoder profile.


### -param pConfig [in]

A pointer to a <a href="https://msdn.microsoft.com/AB963FAD-F16C-47F6-8C78-FF4C234FBC60">D3D11_VIDEO_DECODER_CONFIG</a> structure that specifies the decoder configuration.


### -param ppDecoder [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/F25AFA0B-7413-40F0-AFF8-C9B4549305D2">ID3D11VideoDecoder</a> interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method allocates the necessary decoder buffers. 

The <a href="https://msdn.microsoft.com/dabf52f5-0f69-4017-863c-9e3ecef4d5dc">ID3D11DeviceContext::ClearState</a> method does not affect the internal state of the video decoder.




## -see-also




<a href="https://msdn.microsoft.com/420DE3C4-15A9-4EEB-A1FD-6350DE109CFF">ID3D11VideoDevice</a>
 

 

