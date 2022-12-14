---
UID: NF:d3d10.ID3D10Device.RSSetViewports
title: ID3D10Device::RSSetViewports (d3d10.h)
description: Bind an array of viewports to the rasterizer stage of the pipeline. (ID3D10Device.RSSetViewports)
helpviewer_keywords: ["38205573-be63-f56a-8e33-466b9154f1a9","ID3D10Device interface [Direct3D 10]","RSSetViewports method","ID3D10Device.RSSetViewports","ID3D10Device::RSSetViewports","RSSetViewports","RSSetViewports method [Direct3D 10]","RSSetViewports method [Direct3D 10]","ID3D10Device interface","d3d10/ID3D10Device::RSSetViewports","direct3d10.id3d10device_rssetviewports"]
old-location: direct3d10\id3d10device_rssetviewports.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_rssetviewports.htm
ms.date: 12/05/2018
ms.keywords: 38205573-be63-f56a-8e33-466b9154f1a9, ID3D10Device interface [Direct3D 10],RSSetViewports method, ID3D10Device.RSSetViewports, ID3D10Device::RSSetViewports, RSSetViewports, RSSetViewports method [Direct3D 10], RSSetViewports method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::RSSetViewports, direct3d10.id3d10device_rssetviewports
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
 - ID3D10Device::RSSetViewports
 - d3d10/ID3D10Device::RSSetViewports
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
 - ID3D10Device.RSSetViewports
---

# ID3D10Device::RSSetViewports


## -description

Bind an array of <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage-getting-started">viewports</a> to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage">rasterizer stage</a> of the pipeline.

## -parameters

### -param NumViewports [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of viewports to bind.

### -param pViewports [in]

Type: <b>const <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_viewport">D3D10_VIEWPORT</a>*</b>

An array of viewports (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_viewport">D3D10_VIEWPORT</a>) to bind to the device. Each viewport must have its extents within the allowed ranges: D3D10_VIEWPORT_BOUNDS_MIN, D3D10_VIEWPORT_BOUNDS_MAX, D3D10_MIN_DEPTH, and D3D10_MAX_DEPTH.

## -remarks

All viewports must be set atomically as one operation. Any viewports not defined by the call are disabled.

Which viewport to use is determined by the SV_ViewportArrayIndex semantic output by a geometry shader (see <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics">shader semantic syntax</a>). If a geometry shader does not make use of the SV_ViewportArrayIndex semantic then Direct3D will use the first viewport in the array.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
