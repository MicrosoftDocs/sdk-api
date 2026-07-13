---
UID: NS:d3d12video.D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES
title: D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES
description: Retrieves the list of supported profiles. (D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES)
helpviewer_keywords: ["D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES","D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES",""]
tech.root: mf
ms.assetid: a6721430-bde7-473f-87de-8257bf621a8e
ms.date: 05/28/2019
ms.keywords: D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES, D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES,
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
req.typenames: D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES
targetos: Windows
f1_keywords:
 - D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES
 - d3d12video/D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12video.h
api_name:
 - D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES
---

# D3D12_FEATURE_DATA_VIDEO_DECODE_PROFILES structure


## -description

Provides data for calls to [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12\_FEATURE\_VIDEO\_DECODE\_PROFILES](ne-d3d12video-d3d12_feature_video.md). Retrieves the list of supported profiles.

## -struct-fields

### -field NodeIndex

 
For single GPU operation, set this to zero. If there are multiple GPU nodes, set a bit to identify the node (the device's physical adapter) to which the command queue applies. Each bit in the mask corresponds to a single node. Only 1 bit may be set.

### -field ProfileCount

The number of profiles to retrieve.  This number must match the value returned from a call [ID3D12VideoDevice::CheckFeatureSupport](nf-d3d12video-id3d12videodevice-checkfeaturesupport.md) when the feature specified is [D3D12\_FEATURE\_VIDEO\_DECODE\_PROFILE\_COUNT](ne-d3d12video-d3d12_feature_video.md).

### -field pProfiles

A list of GUIDs representing the supported profiles.  The calling application must allocate storage for the profile list before calling **CheckFeatureSupport**.

## -remarks

## -see-also

[D3D12_FEATURE_VIDEO_DECODE_CONVERSION_SUPPORT](ne-d3d12video-d3d12_feature_video.md)

