---
UID: NF:d3d11.ID3D11VideoContext.ReleaseDecoderBuffer
title: ID3D11VideoContext::ReleaseDecoderBuffer (d3d11.h)
author: windows-sdk-content
description: Releases a buffer that was obtained by calling the ID3D11VideoContext::GetDecoderBuffer method.
old-location: mf\id3d11videocontext_releasedecoderbuffer.htm
tech.root: medfound
ms.assetid: C7BD4CA6-706D-4C3A-AED1-EDF1C65E41E0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext interface [Media Foundation],ReleaseDecoderBuffer method, ID3D11VideoContext.ReleaseDecoderBuffer, ID3D11VideoContext::ReleaseDecoderBuffer, ReleaseDecoderBuffer, ReleaseDecoderBuffer method [Media Foundation], ReleaseDecoderBuffer method [Media Foundation],ID3D11VideoContext interface, d3d11/ID3D11VideoContext::ReleaseDecoderBuffer, mf.id3d11videocontext_releasedecoderbuffer
ms.topic: method
f1_keywords: 
 - "d3d11/ID3D11VideoContext.ReleaseDecoderBuffer"
dev_langs:
 - c++
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
 - ID3D11VideoContext.ReleaseDecoderBuffer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11VideoContext::ReleaseDecoderBuffer


## -description


Releases a buffer that was obtained by calling the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer">ID3D11VideoContext::GetDecoderBuffer</a> method.


## -parameters




### -param pDecoder [in]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder">ID3D11VideoDecoder</a> interface. To get this pointer, call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideodecoder">ID3D11VideoDevice::CreateVideoDecoder</a>.


### -param Type [in]

The type of buffer to release. Specify the same value that was used in the <i>Type</i> parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-getdecoderbuffer">GetDecoderBuffer</a> method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11videocontext">ID3D11VideoContext</a>
 

 

