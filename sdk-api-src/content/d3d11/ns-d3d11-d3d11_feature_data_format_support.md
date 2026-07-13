---
UID: NS:d3d11.D3D11_FEATURE_DATA_FORMAT_SUPPORT
title: D3D11_FEATURE_DATA_FORMAT_SUPPORT (d3d11.h)
description: Describes which resources are supported by the current graphics driver for a given format. (D3D11_FEATURE_DATA_FORMAT_SUPPORT)
helpviewer_keywords: ["D3D11_FEATURE_DATA_FORMAT_SUPPORT","D3D11_FEATURE_DATA_FORMAT_SUPPORT structure [Direct3D 11]","a30c19a0-2294-7e25-009e-e49d1560486d","d3d11/D3D11_FEATURE_DATA_FORMAT_SUPPORT","direct3d11.d3d11_feature_data_format_support"]
old-location: direct3d11\d3d11_feature_data_format_support.htm
tech.root: direct3d11
ms.assetid: 153e246e-9e2f-4557-94c4-a9f1a3b926bd
ms.date: 12/05/2018
ms.keywords: D3D11_FEATURE_DATA_FORMAT_SUPPORT, D3D11_FEATURE_DATA_FORMAT_SUPPORT structure [Direct3D 11], a30c19a0-2294-7e25-009e-e49d1560486d, d3d11/D3D11_FEATURE_DATA_FORMAT_SUPPORT, direct3d11.d3d11_feature_data_format_support
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
req.typenames: D3D11_FEATURE_DATA_FORMAT_SUPPORT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_FEATURE_DATA_FORMAT_SUPPORT
 - d3d11/D3D11_FEATURE_DATA_FORMAT_SUPPORT
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
 - D3D11_FEATURE_DATA_FORMAT_SUPPORT
---

# D3D11_FEATURE_DATA_FORMAT_SUPPORT structure


## -description

Describes which resources are supported by the current graphics driver for a given format.

## -struct-fields

### -field InFormat

Type: <b><a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a></b>


<a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT</a> to return information on.

### -field OutFormatSupport

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Combination of <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_format_support">D3D11_FORMAT_SUPPORT</a> flags indicating which resources are supported.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-structures">Core Structures</a>
