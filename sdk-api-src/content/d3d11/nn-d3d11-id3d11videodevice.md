---
UID: NN:d3d11.ID3D11VideoDevice
title: ID3D11VideoDevice (d3d11.h)
description: Provides the video decoding and video processing capabilities of a Microsoft Direct3D 11 device. (ID3D11VideoDevice)
helpviewer_keywords: ["ID3D11VideoDevice","ID3D11VideoDevice interface [Media Foundation]","ID3D11VideoDevice interface [Media Foundation]","described","d3d11/ID3D11VideoDevice","mf.id3d11videodevice"]
old-location: mf\id3d11videodevice.htm
tech.root: mf
ms.assetid: 420DE3C4-15A9-4EEB-A1FD-6350DE109CFF
ms.date: 12/05/2018
ms.keywords: ID3D11VideoDevice, ID3D11VideoDevice interface [Media Foundation], ID3D11VideoDevice interface [Media Foundation],described, d3d11/ID3D11VideoDevice, mf.id3d11videodevice
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
 - ID3D11VideoDevice
 - d3d11/ID3D11VideoDevice
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
 - ID3D11VideoDevice
---

# ID3D11VideoDevice interface


## -description

Provides the video decoding and video processing capabilities of a Microsoft Direct3D 11 device.

## -inheritance

The <b>ID3D11VideoDevice</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11VideoDevice</b> also has these types of members:

## -remarks

The Direct3D 11 device supports this interface. To get a pointer to this interface, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> with an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a> interface pointer.

If you query an <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a> for <b>ID3D11VideoDevice</b> and the Direct3D 11 device created is using the reference rasterizer or WARP, or is a hardware device and you are using the Microsoft Basic Display Adapter, <b>E_NOINTERFACE</b> is returned.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-interfaces">Direct3D 11 Video Interfaces</a>



<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11videodevice1">ID3D11VideoDevice1</a>
