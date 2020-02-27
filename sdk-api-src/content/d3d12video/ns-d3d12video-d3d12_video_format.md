---
UID: NS:d3d12video.D3D12_VIDEO_FORMAT
title: D3D12_VIDEO_FORMAT
description: Defines the combination of a pixel format and color space for a resource content description.
tech.root: mf
ms.assetid: 83e83e89-fdbf-444b-abea-6a6b62d26ebd
ms.date: 05/28/2019
f1_keywords:
- D3D12_VIDEO_FORMAT
dev_langs:
- c++
ms.keywords: D3D12_VIDEO_FORMAT, D3D12_VIDEO_FORMAT,
req.header: d3d12video.h
req.include-header: 
req.redist: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: d3d12.dll
req.ddi-compliance: 
req.unicode-ansi: 
req.max-support: 
req.typenames: D3D12_VIDEO_FORMAT
topic_type:
- apiref
api_type:
- HeaderDef
api_location:
- d3d12video.h
api_name:
- D3D12_VIDEO_FORMAT
targetos: Windows
---

# D3D12_VIDEO_FORMAT structure

## -description

Defines the combination of a pixel format and color space for a resource content description.

## -struct-fields

### -field Format

A value from the [DXGI_FORMAT](https://docs.microsoft.com/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enumeration, specifying the DXGI format of the data.
 
### -field ColorSpace
 
A value from the [DXGI_COLOR_SPACE_TYPE](https://docs.microsoft.com/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) enumeration, specifying the color space of the data.

## -remarks

## -see-also
