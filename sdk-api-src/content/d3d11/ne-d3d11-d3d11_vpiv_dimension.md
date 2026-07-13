---
UID: NE:d3d11.D3D11_VPIV_DIMENSION
title: D3D11_VPIV_DIMENSION (d3d11.h)
description: Specifies how to access a resource that is used in a video processor input view.
helpviewer_keywords: ["D3D11_VPIV_DIMENSION","D3D11_VPIV_DIMENSION enumeration [Media Foundation]","D3D11_VPIV_DIMENSION_TEXTURE2D","D3D11_VPIV_DIMENSION_UNKNOWN","d3d11/D3D11_VPIV_DIMENSION","d3d11/D3D11_VPIV_DIMENSION_TEXTURE2D","d3d11/D3D11_VPIV_DIMENSION_UNKNOWN","mf.d3d11_vpiv_dimension"]
old-location: mf\d3d11_vpiv_dimension.htm
tech.root: mf
ms.assetid: 65003974-F86E-4604-BA8D-262CA2674D53
ms.date: 12/05/2018
ms.keywords: D3D11_VPIV_DIMENSION, D3D11_VPIV_DIMENSION enumeration [Media Foundation], D3D11_VPIV_DIMENSION_TEXTURE2D, D3D11_VPIV_DIMENSION_UNKNOWN, d3d11/D3D11_VPIV_DIMENSION, d3d11/D3D11_VPIV_DIMENSION_TEXTURE2D, d3d11/D3D11_VPIV_DIMENSION_UNKNOWN, mf.d3d11_vpiv_dimension
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
req.typenames: D3D11_VPIV_DIMENSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_VPIV_DIMENSION
 - d3d11/D3D11_VPIV_DIMENSION
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
 - D3D11_VPIV_DIMENSION
---

# D3D11_VPIV_DIMENSION enumeration


## -description

Specifies how to access a resource that is used in a video processor input view.

## -enum-fields

### -field D3D11_VPIV_DIMENSION_UNKNOWN:0

Not a valid value.

### -field D3D11_VPIV_DIMENSION_TEXTURE2D:1

The resource will be accessed as a 2D texture.

## -remarks

This enumeration is used with the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_input_view_desc">D3D11_VIDEO_PROCESSOR_INPUT_VIEW_DESC</a> structure.

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-enumerations">Direct3D 11 Video Enumerations</a>



<a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videodevice-createvideoprocessorinputview">ID3D11VideoDevice::CreateVideoProcessorInputView</a>
