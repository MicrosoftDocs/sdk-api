---
UID: NF:d3d10.ID3D10Device.VSSetShader
title: ID3D10Device::VSSetShader (d3d10.h)
description: Set a vertex shader to the device. (ID3D10Device.VSSetShader)
helpviewer_keywords: ["8aebab54-e44a-a11b-1d07-449a345b9922","ID3D10Device interface [Direct3D 10]","VSSetShader method","ID3D10Device.VSSetShader","ID3D10Device::VSSetShader","VSSetShader","VSSetShader method [Direct3D 10]","VSSetShader method [Direct3D 10]","ID3D10Device interface","d3d10/ID3D10Device::VSSetShader","direct3d10.id3d10device_vssetshader"]
old-location: direct3d10\id3d10device_vssetshader.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_vssetshader.htm
ms.date: 12/05/2018
ms.keywords: 8aebab54-e44a-a11b-1d07-449a345b9922, ID3D10Device interface [Direct3D 10],VSSetShader method, ID3D10Device.VSSetShader, ID3D10Device::VSSetShader, VSSetShader, VSSetShader method [Direct3D 10], VSSetShader method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::VSSetShader, direct3d10.id3d10device_vssetshader
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
 - ID3D10Device::VSSetShader
 - d3d10/ID3D10Device::VSSetShader
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
 - ID3D10Device.VSSetShader
---

# ID3D10Device::VSSetShader


## -description

Set a vertex shader to the device.

## -parameters

### -param pVertexShader [in]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10vertexshader">ID3D10VertexShader</a>*</b>

Pointer to a vertex shader (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10vertexshader">ID3D10VertexShader</a>). Passing in <b>NULL</b> disables the shader for this pipeline stage.

## -remarks

The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an interface currently in use by the device.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
