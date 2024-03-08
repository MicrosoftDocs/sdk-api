---
UID: NF:d3d10.ID3D10Device.OMSetDepthStencilState
title: ID3D10Device::OMSetDepthStencilState (d3d10.h)
description: Sets the depth-stencil state of the output-merger stage. (ID3D10Device.OMSetDepthStencilState)
helpviewer_keywords: ["75af58f4-0720-3b37-1633-f4ae71d23ebd","ID3D10Device interface [Direct3D 10]","OMSetDepthStencilState method","ID3D10Device.OMSetDepthStencilState","ID3D10Device::OMSetDepthStencilState","OMSetDepthStencilState","OMSetDepthStencilState method [Direct3D 10]","OMSetDepthStencilState method [Direct3D 10]","ID3D10Device interface","d3d10/ID3D10Device::OMSetDepthStencilState","direct3d10.id3d10device_omsetdepthstencilstate"]
old-location: direct3d10\id3d10device_omsetdepthstencilstate.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_omsetdepthstencilstate.htm
ms.date: 12/05/2018
ms.keywords: 75af58f4-0720-3b37-1633-f4ae71d23ebd, ID3D10Device interface [Direct3D 10],OMSetDepthStencilState method, ID3D10Device.OMSetDepthStencilState, ID3D10Device::OMSetDepthStencilState, OMSetDepthStencilState, OMSetDepthStencilState method [Direct3D 10], OMSetDepthStencilState method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::OMSetDepthStencilState, direct3d10.id3d10device_omsetdepthstencilstate
req.header: d3d10.h
req.include-header: 
req.target-type: Windows
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Device::OMSetDepthStencilState
 - d3d10/ID3D10Device::OMSetDepthStencilState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Device.OMSetDepthStencilState
---

# ID3D10Device::OMSetDepthStencilState


## -description

Sets the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">depth-stencil</a> state of 
    the output-merger stage.

## -parameters

### -param pDepthStencilState [in]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10depthstencilstate">ID3D10DepthStencilState</a>*</b>

Pointer to a depth-stencil state interface (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10depthstencilstate">ID3D10DepthStencilState</a>) to bind to the device.

### -param StencilRef [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Reference value to perform against when doing a depth-stencil test. See remarks.

## -remarks

To create a depth-stencil state interface, call <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createdepthstencilstate">ID3D10Device::CreateDepthStencilState</a>.

Depth-stencil state is used by the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-output-merger-stage">output-merger</a> stage to 
      setup depth-stencil testing. 
      The stencil reference value is the control value used in the depth-stencil test.

The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an 
      interface currently in use by the device.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
