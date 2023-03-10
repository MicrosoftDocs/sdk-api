---
UID: NF:d3d11.ID3D11Device.CheckFeatureSupport
title: ID3D11Device::CheckFeatureSupport (d3d11.h)
description: Gets information about the features that are supported by the current graphics driver. (ID3D11Device.CheckFeatureSupport)
helpviewer_keywords: ["CheckFeatureSupport","CheckFeatureSupport method [Direct3D 11]","CheckFeatureSupport method [Direct3D 11]","ID3D11Device interface","ID3D11Device interface [Direct3D 11]","CheckFeatureSupport method","ID3D11Device.CheckFeatureSupport","ID3D11Device::CheckFeatureSupport","cf1b66c2-5336-35b5-28c8-154fc99a01ee","d3d11/ID3D11Device::CheckFeatureSupport","direct3d11.id3d11device_checkfeaturesupport"]
old-location: direct3d11\id3d11device_checkfeaturesupport.htm
tech.root: direct3d11
ms.assetid: 7edf2ffd-908a-4cf8-9ac6-8fd14d7a0ea1
ms.date: 12/05/2018
ms.keywords: CheckFeatureSupport, CheckFeatureSupport method [Direct3D 11], CheckFeatureSupport method [Direct3D 11],ID3D11Device interface, ID3D11Device interface [Direct3D 11],CheckFeatureSupport method, ID3D11Device.CheckFeatureSupport, ID3D11Device::CheckFeatureSupport, cf1b66c2-5336-35b5-28c8-154fc99a01ee, d3d11/ID3D11Device::CheckFeatureSupport, direct3d11.id3d11device_checkfeaturesupport
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3d11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Device::CheckFeatureSupport
 - d3d11/ID3D11Device::CheckFeatureSupport
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.lib
 - d3d11.dll
api_name:
 - ID3D11Device.CheckFeatureSupport
---

# ID3D11Device::CheckFeatureSupport


## -description

Gets information about the features that are supported by the current graphics driver.

## -parameters

### -param Feature

Type: <b><a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature">D3D11_FEATURE</a></b>

A member of the <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature">D3D11_FEATURE</a> enumerated type that describes which feature to query for support.

### -param pFeatureSupportData [out]

Type: <b>void*</b>

Upon completion of the method, the passed structure is filled with data that describes the feature support.

### -param FeatureSupportDataSize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The size of the structure passed to the <i>pFeatureSupportData</i> parameter.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns E_INVALIDARG if an unsupported data type is passed to the <i>pFeatureSupportData</i> parameter 
      or a size mismatch is detected for the <i>FeatureSupportDataSize</i> parameter.

## -remarks

To query for multi-threading support, pass the <b>D3D11_FEATURE_THREADING</b> value to the <i>Feature</i> parameter, pass 
      the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_threading">D3D11_FEATURE_DATA_THREADING</a> structure to the  <i>pFeatureSupportData</i> parameter, and pass the size of 
      the <b>D3D11_FEATURE_DATA_THREADING</b> structure to the <i>FeatureSupportDataSize</i> parameter.

Calling CheckFeatureSupport with <i>Feature</i> set to D3D11_FEATURE_FORMAT_SUPPORT causes the method to return the same information that would be returned 
      by <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkformatsupport">ID3D11Device::CheckFormatSupport</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a>
