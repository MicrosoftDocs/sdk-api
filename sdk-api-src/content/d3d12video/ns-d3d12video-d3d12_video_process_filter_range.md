---
UID: NS:d3d12video.D3D12_VIDEO_PROCESS_FILTER_RANGE
title: D3D12_VIDEO_PROCESS_FILTER_RANGE
description: Defines the range of supported values for an image filter. (D3D12_VIDEO_PROCESS_FILTER_RANGE)
helpviewer_keywords: ["D3D12_VIDEO_PROCESS_FILTER_RANGE","D3D12_VIDEO_PROCESS_FILTER_RANGE",""]
tech.root: mf
ms.assetid: d9effd83-7420-45be-b360-eea63db64d1c
ms.date: 05/28/2019
ms.keywords: D3D12_VIDEO_PROCESS_FILTER_RANGE, D3D12_VIDEO_PROCESS_FILTER_RANGE,
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
req.typenames: D3D12_VIDEO_PROCESS_FILTER_RANGE
targetos: Windows
f1_keywords:
 - D3D12_VIDEO_PROCESS_FILTER_RANGE
 - d3d12video/D3D12_VIDEO_PROCESS_FILTER_RANGE
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_VIDEO_PROCESS_FILTER_RANGE
---

# D3D12_VIDEO_PROCESS_FILTER_RANGE structure


## -description

Defines the range of supported values for an image filter.

## -struct-fields

### -field Minimum

The minimum value of the filter.

### -field Maximum

The maximum value of the filter.

### -field Default

The default value of the filter.

### -field Multiplier

 
A multiplier. Use the following formula to translate the filter setting into the actual filter value: 

`Actual Value = Set Value × Multiplier.`

## -remarks

The multiplier enables the filter range to have a fractional step value. For example, a hue filter might have an actual range of [–180.0 ... +180.0] with a step size of 0.25. The device would report the following range and multiplier:

- Minimum: –720
- Maximum: +720
- Multiplier: 0.25

In this case, a filter value of 2 would be interpreted by the device as 0.50 (or 2 × 0.25).

The device should use a multiplier that can be represented exactly as a base-2 fraction.

## -see-also

