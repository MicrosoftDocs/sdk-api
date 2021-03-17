---
UID: NF:d3d10.ID3D10Device.RSGetViewports
title: ID3D10Device::RSGetViewports (d3d10.h)
description: Get the array of viewports bound to the rasterizer stage
helpviewer_keywords: ["ID3D10Device interface [Direct3D 10]","RSGetViewports method","ID3D10Device.RSGetViewports","ID3D10Device::RSGetViewports","RSGetViewports","RSGetViewports method [Direct3D 10]","RSGetViewports method [Direct3D 10]","ID3D10Device interface","d3d10/ID3D10Device::RSGetViewports","d9ea7cbf-16e9-686e-f682-4c7619caae2c","direct3d10.id3d10device_rsgetviewports"]
old-location: direct3d10\id3d10device_rsgetviewports.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_rsgetviewports.htm
ms.date: 12/05/2018
ms.keywords: ID3D10Device interface [Direct3D 10],RSGetViewports method, ID3D10Device.RSGetViewports, ID3D10Device::RSGetViewports, RSGetViewports, RSGetViewports method [Direct3D 10], RSGetViewports method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::RSGetViewports, d9ea7cbf-16e9-686e-f682-4c7619caae2c, direct3d10.id3d10device_rsgetviewports
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
 - ID3D10Device::RSGetViewports
 - d3d10/ID3D10Device::RSGetViewports
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
 - ID3D10Device.RSGetViewports
---

# ID3D10Device::RSGetViewports


## -description

Get the array of <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage-getting-started">viewports</a> bound 
    to the <a href="/windows/desktop/direct3d11/d3d10-graphics-programming-guide-rasterizer-stage">rasterizer stage</a>

## -parameters

### -param NumViewports [in, out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

Number of viewports in <i>pViewports</i>.  
        If <i>pViewports</i> is <b>NULL</b>, this will be filled with the number of viewports currently bound.

### -param pViewports [out]

Type: <b><a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_viewport">D3D10_VIEWPORT</a>*</b>

An array of viewports (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_viewport">D3D10_VIEWPORT</a>) to be filled with information from the device. If NumViewports is greater than 
        the actual number of viewports currently bound, then unused members of the array will contain 0.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>