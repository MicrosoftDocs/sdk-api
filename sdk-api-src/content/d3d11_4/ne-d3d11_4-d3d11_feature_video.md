---
UID: NE:d3d11_4.D3D11_FEATURE_VIDEO
title: D3D11_FEATURE_VIDEO
description: Specifies a Direct3D 11 video feature or feature set to query about.
helpviewer_keywords: ["D3D11_FEATURE_VIDEO"]
tech.root: mf
ms.date: 4/26/2019
ms.keywords: D3D11_FEATURE_VIDEO
targetos: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: d3d11_4.h
req.include-header: 
req.lib: D3d11.lib
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: 
req.umdf-ver: 
f1_keywords:
 - D3D11_FEATURE_VIDEO
 - d3d11_4/D3D11_FEATURE_VIDEO
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d11_4.h
api_name:
 - D3D11_FEATURE_VIDEO
---

## -description

Specifies a Direct3D 11 video feature or feature set to query about. When you want to query for the level to which an adapter supports a feature, pass one of these values to <a href = "nf-d3d11_4-id3d11videodevice2-checkfeaturesupport.md">ID3D11VideoDevice2::CheckFeatureSupport</a>.

## -enum-fields

### -field D3D11_FEATURE_VIDEO_DECODER_HISTOGRAM:0

Retrieves the supported components, bin count, and counter bit depth for the a decode histogram with the specified decode profile, resolution, and format. The associated data structure is <a href ="ns-d3d11_4-d3d11_feature_data_video_decoder_histogram.md">D3D11_FEATURE_DATA_VIDEO_DECODER_HISTOGRAM</a>.

## -remarks

## -see-also

<a href = "nf-d3d11_4-id3d11videodevice2-checkfeaturesupport.md">ID3D11VideoDevice2::CheckFeatureSupport</a>

