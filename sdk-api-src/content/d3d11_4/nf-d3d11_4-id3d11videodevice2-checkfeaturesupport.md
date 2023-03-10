---
UID: NF:d3d11_4.ID3D11VideoDevice2.CheckFeatureSupport
title: ID3D11VideoDevice2::CheckFeatureSupport
description: Gets information about the features that are supported by the current video driver. (ID3D11VideoDevice2::CheckFeatureSupport)
tech.root: direct3d11
helpviewer_keywords: ["ID3D11VideoDevice2::CheckFeatureSupport"]
ms.date: 4/26/2019
ms.keywords: ID3D11VideoDevice2::CheckFeatureSupport
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: d3d11_4.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - ID3D11VideoDevice2::CheckFeatureSupport
 - d3d11_4/ID3D11VideoDevice2::CheckFeatureSupport
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d11_4.h
api_name:
 - ID3D11VideoDevice2::CheckFeatureSupport
---

## -description

Gets information about the features that are supported by the current video driver.

## -parameters

### -param Feature

A member of the [D3D11_FEATURE_VIDEO](ne-d3d11_4-d3d11_feature_video.md) enumeration that specifies the feature to query for support.

### -param pFeatureSupportData

A structure that contains data that describes the configuration details of the feature for which support is requested and, upon the completion of the call, is populated with details about the level of support available. For information on the structure that is associated with each type of feature support request, see the field descriptions for [D3D11_FEATURE_VIDEO](ne-d3d11_4-d3d11_feature_video.md).

### -param FeatureSupportDataSize

The size of the structure passed to the *pFeatureSupportData* parameter.

## -returns

Returns **S_OK** if successful; otherwise, returns **E_INVALIDARG** if an unsupported data type is passed to the *pFeatureSupportData* parameter or a size mismatch is detected for the *FeatureSupportDataSize* parameter.

## -remarks

## -see-also

[D3D11_FEATURE_VIDEO](ne-d3d11_4-d3d11_feature_video.md)

