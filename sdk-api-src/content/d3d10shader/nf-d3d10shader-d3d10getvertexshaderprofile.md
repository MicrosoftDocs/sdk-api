---
UID: NF:d3d10shader.D3D10GetVertexShaderProfile
title: D3D10GetVertexShaderProfile function (d3d10shader.h)
description: Get the vertex shader profile best suited to a given device.
helpviewer_keywords: ["D3D10GetVertexShaderProfile","D3D10GetVertexShaderProfile function [Direct3D 10]","d3d10shader/D3D10GetVertexShaderProfile","direct3d10.d3d10getvertexshaderprofile","ed448170-9ae1-2f57-6e8e-b9cf7adec9c1"]
old-location: direct3d10\d3d10getvertexshaderprofile.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10getvertexshaderprofile.htm
ms.date: 12/05/2018
ms.keywords: D3D10GetVertexShaderProfile, D3D10GetVertexShaderProfile function [Direct3D 10], d3d10shader/D3D10GetVertexShaderProfile, direct3d10.d3d10getvertexshaderprofile, ed448170-9ae1-2f57-6e8e-b9cf7adec9c1
req.header: d3d10shader.h
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
req.dll: D3D10.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10GetVertexShaderProfile
 - d3d10shader/D3D10GetVertexShaderProfile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3D10.dll
api_name:
 - D3D10GetVertexShaderProfile
---

# D3D10GetVertexShaderProfile function


## -description

Get the vertex <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-models">shader profile</a> best suited to a given device.

## -parameters

### -param pDevice [in]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a>*</b>

Pointer to the device (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>).

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The shader profile.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-functions">Shader Functions</a>