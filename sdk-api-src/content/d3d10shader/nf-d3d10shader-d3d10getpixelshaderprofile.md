---
UID: NF:d3d10shader.D3D10GetPixelShaderProfile
title: D3D10GetPixelShaderProfile function (d3d10shader.h)
description: Get the pixel shader profile best suited to a given device.
helpviewer_keywords: ["8d581e0e-4553-6a9c-455b-9ef399e0d29f","D3D10GetPixelShaderProfile","D3D10GetPixelShaderProfile function [Direct3D 10]","d3d10shader/D3D10GetPixelShaderProfile","direct3d10.d3d10getpixelshaderprofile"]
old-location: direct3d10\d3d10getpixelshaderprofile.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10getpixelshaderprofile.htm
ms.date: 12/05/2018
ms.keywords: 8d581e0e-4553-6a9c-455b-9ef399e0d29f, D3D10GetPixelShaderProfile, D3D10GetPixelShaderProfile function [Direct3D 10], d3d10shader/D3D10GetPixelShaderProfile, direct3d10.d3d10getpixelshaderprofile
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
 - D3D10GetPixelShaderProfile
 - d3d10shader/D3D10GetPixelShaderProfile
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
 - D3D10GetPixelShaderProfile
---

# D3D10GetPixelShaderProfile function


## -description

Get the pixel <a href="/windows/desktop/direct3dhlsl/dx-graphics-hlsl-models">shader profile</a> best suited to a given device.

## -parameters

### -param pDevice [in]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device</a>*</b>

Pointer to the device (see <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>).

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The shader profile.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-functions">Shader Functions</a>