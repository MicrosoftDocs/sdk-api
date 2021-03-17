---
UID: NS:d3d12video.D3D12_VIDEO_SIZE_RANGE
title: D3D12_VIDEO_SIZE_RANGE
description: Describes the range of supported sizes for a video scaler.
helpviewer_keywords: ["D3D12_VIDEO_SIZE_RANGE","D3D12_VIDEO_SIZE_RANGE",""]
tech.root: mf
ms.assetid: 1dc0ed58-ae25-4c19-81a8-74fd0ad83580
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_SIZE_RANGE, D3D12_VIDEO_SIZE_RANGE,
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
req.typenames: D3D12_VIDEO_SIZE_RANGE
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_SIZE_RANGE
 - d3d12video/D3D12_VIDEO_SIZE_RANGE
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_SIZE_RANGE
---

# D3D12_VIDEO_SIZE_RANGE structure


## -description

Describes the range of supported sizes for a video scaler.

## -struct-fields

### -field MaxWidth

 
The largest output width to which content can be scaled.  The largest value allowed is **D3D12\_REQ\_TEXTURE2D\_U\_OR\_V\_DIMENSION** (16384).

### -field MaxHeight

The largest output height to which content can be scaled.  The largest value allowed is **D3D12\_REQ\_TEXTURE2D\_U\_OR\_V\_DIMENSION** (16384).

### -field MinWidth

The smallest output width to which content can be scaled. The smallest allowed value is 1.

### -field MinHeight

 
The smallest output height to which content can be scaled. The smallest allowed value is 1.

## -remarks

## -see-also

