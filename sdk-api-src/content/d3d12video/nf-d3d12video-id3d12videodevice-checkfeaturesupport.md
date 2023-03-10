---
UID: NF:d3d12video.ID3D12VideoDevice.CheckFeatureSupport
title: ID3D12VideoDevice::CheckFeatureSupport
description: Gets information about the features that are supported by the current video driver. (ID3D12VideoDevice::CheckFeatureSupport)
helpviewer_keywords: ["ID3D12VideoDevice::CheckFeatureSupport","CheckFeatureSupport","ID3D12VideoDevice.CheckFeatureSupport","ID3D12VideoDevice::CheckFeatureSupport","ID3D12VideoDevice.CheckFeatureSupport"]
tech.root: mf
ms.assetid: 9386573a-29f0-478e-9803-3773d93eea4a
ms.date: 05/28/2019
ms.keywords: ID3D12VideoDevice::CheckFeatureSupport, CheckFeatureSupport, ID3D12VideoDevice.CheckFeatureSupport, ID3D12VideoDevice::CheckFeatureSupport, ID3D12VideoDevice.CheckFeatureSupport
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
req.irql: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
f1_keywords:
 - ID3D12VideoDevice::CheckFeatureSupport
 - d3d12video/ID3D12VideoDevice::CheckFeatureSupport
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12VideoDevice::CheckFeatureSupport
---

# ID3D12VideoDevice::CheckFeatureSupport


## -description

Gets information about the features that are supported by the current video driver.

## -parameters

### -param FeatureVideo

A member of the [D3D12\_FEATURE\_VIDEO](ne-d3d12video-d3d12_feature_video.md) enumeration that specifies the feature to query for support.

### -param pFeatureSupportData

A structure that contains data that describes the configuration details of the feature for which support is requested and, upon the completion of the call, is populated with details about the level of support available. For information on the structure that is associated with each type of feature support request, see the field descriptions for [D3D12\_FEATURE\_VIDEO](ne-d3d12video-d3d12_feature_video.md).

### -param FeatureSupportDataSize

The size of the structure passed to the *pFeatureSupportData* parameter.

## -returns

Returns **S\_OK** if successful; otherwise, returns **E\_INVALIDARG** if an unsupported data type is passed to the *pFeatureSupportData* parameter or a size mismatch is detected for the *FeatureSupportDataSize* parameter.

## -remarks

## -see-also

