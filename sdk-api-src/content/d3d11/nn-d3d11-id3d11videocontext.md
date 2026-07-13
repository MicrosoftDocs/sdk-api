---
UID: NN:d3d11.ID3D11VideoContext
title: ID3D11VideoContext (d3d11.h)
description: Provides the video functionality of a Microsoft Direct3D 11 device. (ID3D11VideoContext)
helpviewer_keywords: ["ID3D11VideoContext","ID3D11VideoContext interface [Media Foundation]","ID3D11VideoContext interface [Media Foundation]","described","d3d11/ID3D11VideoContext","mf.id3d11videocontext"]
old-location: mf\id3d11videocontext.htm
tech.root: mf
ms.assetid: 6EF09C31-56C7-46B5-87AE-B1FE43EC66FC
ms.date: 12/05/2018
ms.keywords: ID3D11VideoContext, ID3D11VideoContext interface [Media Foundation], ID3D11VideoContext interface [Media Foundation],described, d3d11/ID3D11VideoContext, mf.id3d11videocontext
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11VideoContext
 - d3d11/ID3D11VideoContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoContext
---

# ID3D11VideoContext interface


## -description

Provides the video functionality of a Microsoft Direct3D 11 device.

## -inheritance

The <b>ID3D11VideoContext</b> interface inherits from <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>. <b>ID3D11VideoContext</b> also has these types of members:

## -remarks

To get a pointer to this interface, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> with an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a> interface pointer.

This interface provides access to several areas of Microsoft Direct3Dvideo functionality:

<ul>
<li>Hardware-accelerated video decoding</li>
<li>Video processing</li>
<li>GPU-based content protection</li>
<li>Video encryption and decryption</li>
</ul>
In Microsoft Direct3D 9, the equivalent functions were distributed across several interfaces:

<ul>
<li>
<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3dauthenticatedchannel9">IDirect3DAuthenticatedChannel9</a>
</li>
<li>
<a href="/windows/desktop/api/d3d9/nn-d3d9-idirect3dcryptosession9">IDirect3DCryptoSession9</a>
</li>
<li>
<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder">IDirectXVideoDecoder</a>
</li>
<li>
<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor">IDirectXVideoProcessor</a>
</li>
<li>
<a href="/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor">IDXVAHD_VideoProcessor</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-interfaces">Direct3D 11 Video Interfaces</a>



<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicechild">ID3D11DeviceChild</a>



<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11videocontext1">ID3D11VideoContext1</a>
