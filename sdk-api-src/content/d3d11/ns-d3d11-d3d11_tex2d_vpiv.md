---
UID: NS:d3d11.D3D11_TEX2D_VPIV
title: D3D11_TEX2D_VPIV (d3d11.h)
description: Identifies the texture resource for a video processor input view.
helpviewer_keywords: ["D3D11_TEX2D_VPIV","D3D11_TEX2D_VPIV structure [Media Foundation]","d3d11/D3D11_TEX2D_VPIV","mf.d3d11_tex2d_vpiv"]
old-location: mf\d3d11_tex2d_vpiv.htm
tech.root: mf
ms.assetid: F174DF16-6E2F-4AE1-80D9-7565F96DE03A
ms.date: 12/05/2018
ms.keywords: D3D11_TEX2D_VPIV, D3D11_TEX2D_VPIV structure [Media Foundation], d3d11/D3D11_TEX2D_VPIV, mf.d3d11_tex2d_vpiv
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
req.typenames: D3D11_TEX2D_VPIV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TEX2D_VPIV
 - d3d11/D3D11_TEX2D_VPIV
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_TEX2D_VPIV
---

# D3D11_TEX2D_VPIV structure


## -description

Identifies the texture resource for a video  processor input view.

## -struct-fields

### -field MipSlice

The zero-based index into the array of subtextures.

### -field ArraySlice

The zero-based index of the texture.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>



<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessorinputview">ID3D11VideoDevice::CreateVideoProcessorInputView</a>