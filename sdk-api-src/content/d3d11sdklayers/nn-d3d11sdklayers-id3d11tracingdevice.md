---
UID: NN:d3d11sdklayers.ID3D11TracingDevice
title: ID3D11TracingDevice (d3d11sdklayers.h)
description: The tracing device interface sets shader tracking information, which enables accurate logging and playback of shader execution.
helpviewer_keywords: ["ID3D11TracingDevice","ID3D11TracingDevice interface [Direct3D 11]","ID3D11TracingDevice interface [Direct3D 11]","described","d3d11sdklayers/ID3D11TracingDevice","direct3d11.id3d11tracingdevice"]
old-location: direct3d11\id3d11tracingdevice.htm
tech.root: direct3d11
ms.assetid: AE42E2A8-9FEE-4991-B1A0-4C6C04958DE4
ms.date: 12/05/2018
ms.keywords: ID3D11TracingDevice, ID3D11TracingDevice interface [Direct3D 11], ID3D11TracingDevice interface [Direct3D 11],described, d3d11sdklayers/ID3D11TracingDevice, direct3d11.id3d11tracingdevice
req.header: d3d11sdklayers.h
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
req.lib: D3DCompiler.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11TracingDevice
 - d3d11sdklayers/ID3D11TracingDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler.lib
 - D3DCompiler.dll
api_name:
 - ID3D11TracingDevice
---

# ID3D11TracingDevice interface


## -description

The tracing device interface sets shader tracking information, which enables accurate logging and playback of shader execution.

## -inheritance

The <b>ID3D11TracingDevice</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11TracingDevice</b> also has these types of members:

## -remarks

To get this interface, turn on the <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers">debug layer</a> and use <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> from the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>.

<div class="alert"><b>Note</b>  This API requires the Windows Software Development Kit (SDK) for Windows 8.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-layer-interfaces">Layer Interfaces</a>
