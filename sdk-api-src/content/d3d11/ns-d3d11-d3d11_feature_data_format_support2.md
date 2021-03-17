---
UID: NS:d3d11.D3D11_FEATURE_DATA_FORMAT_SUPPORT2
title: D3D11_FEATURE_DATA_FORMAT_SUPPORT2 (d3d11.h)
description: Describes which unordered resource options are supported by the current graphics driver for a given format.
helpviewer_keywords: ["666f73ad-8c04-9774-e3ed-01d758bb509f","D3D11_FEATURE_DATA_FORMAT_SUPPORT2","D3D11_FEATURE_DATA_FORMAT_SUPPORT2 structure [Direct3D 11]","d3d11/D3D11_FEATURE_DATA_FORMAT_SUPPORT2","direct3d11.d3d11_feature_data_format_support2"]
old-location: direct3d11\d3d11_feature_data_format_support2.htm
tech.root: direct3d11
ms.assetid: 075cc44a-3c91-4015-af7f-489b3b3c6661
ms.date: 12/05/2018
ms.keywords: 666f73ad-8c04-9774-e3ed-01d758bb509f, D3D11_FEATURE_DATA_FORMAT_SUPPORT2, D3D11_FEATURE_DATA_FORMAT_SUPPORT2 structure [Direct3D 11], d3d11/D3D11_FEATURE_DATA_FORMAT_SUPPORT2, direct3d11.d3d11_feature_data_format_support2
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D11_FEATURE_DATA_FORMAT_SUPPORT2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_FEATURE_DATA_FORMAT_SUPPORT2
 - d3d11/D3D11_FEATURE_DATA_FORMAT_SUPPORT2
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
 - D3D11_FEATURE_DATA_FORMAT_SUPPORT2
---

# D3D11_FEATURE_DATA_FORMAT_SUPPORT2 structure


## -description

Describes which unordered resource options are supported by the current graphics driver for a given format.

## -struct-fields

### -field InFormat

Type: <b><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a></b>


<a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> to return information on.

### -field OutFormatSupport2

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Combination of <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support2">D3D11_FORMAT_SUPPORT2</a> flags indicating which unordered resource options are supported.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-structures">Core Structures</a>