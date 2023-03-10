---
UID: NS:d3d11.D3D11_FEATURE_DATA_MARKER_SUPPORT
title: D3D11_FEATURE_DATA_MARKER_SUPPORT (d3d11.h)
description: Describes whether a GPU profiling technique is supported.
helpviewer_keywords: ["D3D11_FEATURE_DATA_MARKER_SUPPORT","D3D11_FEATURE_DATA_MARKER_SUPPORT structure [Direct3D 11]","d3d11/D3D11_FEATURE_DATA_MARKER_SUPPORT","direct3d11.d3d11_feature_data_marker_support"]
old-location: direct3d11\d3d11_feature_data_marker_support.htm
tech.root: direct3d11
ms.assetid: 950381BB-E8F6-416D-8F36-CC3591E71703
ms.date: 12/05/2018
ms.keywords: D3D11_FEATURE_DATA_MARKER_SUPPORT, D3D11_FEATURE_DATA_MARKER_SUPPORT structure [Direct3D 11], d3d11/D3D11_FEATURE_DATA_MARKER_SUPPORT, direct3d11.d3d11_feature_data_marker_support
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
req.typenames: D3D11_FEATURE_DATA_MARKER_SUPPORT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_FEATURE_DATA_MARKER_SUPPORT
 - d3d11/D3D11_FEATURE_DATA_MARKER_SUPPORT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_FEATURE_DATA_MARKER_SUPPORT
---

# D3D11_FEATURE_DATA_MARKER_SUPPORT structure


## -description

<div class="alert"><b>Note</b>  This structure is supported by the Direct3D 11.2 runtime, which is available on Windows 8.1 and later operating systems.</div><div> </div>Describes whether a GPU profiling technique is supported.

## -struct-fields

### -field Profile

Specifies whether the hardware and driver support a GPU profiling technique that can be used with development tools. The runtime sets this member to <b>TRUE</b> if  the hardware and driver support data marking.

## -remarks

If the Direct3D API is the Direct3D 11.2 runtime and can support 11.2 features, <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport">ID3D11Device::CheckFeatureSupport</a> for <b>D3D11_FEATURE_MARKER_SUPPORT</b> will return a SUCCESS code when valid parameters are passed. The <b>Profile</b> member of <b>D3D11_FEATURE_DATA_MARKER_SUPPORT</b> will be set to <b>TRUE</b> or <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-structures">Core Structures</a>



<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature">D3D11_FEATURE</a>