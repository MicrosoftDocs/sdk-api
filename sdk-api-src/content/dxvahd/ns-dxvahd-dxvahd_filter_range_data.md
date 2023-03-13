---
UID: NS:dxvahd._DXVAHD_FILTER_RANGE_DATA
title: DXVAHD_FILTER_RANGE_DATA (dxvahd.h)
description: Defines the range of supported values for an image filter. (DXVAHD_FILTER_RANGE_DATA)
helpviewer_keywords: ["DXVAHD_FILTER_RANGE_DATA","DXVAHD_FILTER_RANGE_DATA structure [Media Foundation]","dxvahd/DXVAHD_FILTER_RANGE_DATA","mf.dxvahd_filter_range_data"]
old-location: mf\dxvahd_filter_range_data.htm
tech.root: mf
ms.assetid: cd349ac5-9825-4dc8-8735-5d846abb353b
ms.date: 12/05/2018
ms.keywords: DXVAHD_FILTER_RANGE_DATA, DXVAHD_FILTER_RANGE_DATA structure [Media Foundation], dxvahd/DXVAHD_FILTER_RANGE_DATA, mf.dxvahd_filter_range_data
req.header: dxvahd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: DXVAHD_FILTER_RANGE_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DXVAHD_FILTER_RANGE_DATA
 - dxvahd/_DXVAHD_FILTER_RANGE_DATA
 - DXVAHD_FILTER_RANGE_DATA
 - dxvahd/DXVAHD_FILTER_RANGE_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxvahd.h
api_name:
 - DXVAHD_FILTER_RANGE_DATA
---

# DXVAHD_FILTER_RANGE_DATA structure


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

A multiplier. Use the following formula to translate the filter setting into the actual filter value: <i>Actual Value</i> = <i>Set Value</i> × <i>Multiplier</i>.

## -remarks

The multiplier enables the filter range to have a fractional step value.

For example, a hue filter might have an actual range of [-180.0 ... +180.0] with a step size of 0.25. The device would report the following range and multiplier:

<ul>
<li>Minimum: -720</li>
<li>Maximum: +720</li>
<li>Multiplier: 0.25</li>
</ul>
In this case,  a filter value of 2 would be interpreted by the device as 0.50 (or 2 × 0.25).

The device should use  a multiplier that can be represented exactly as a base-2 fraction.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/medfound/direct3d-video-structures">Direct3D Video Structures</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>
