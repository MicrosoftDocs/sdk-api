---
UID: NS:d3d11_4.D3D11_FEATURE_DATA_D3D11_OPTIONS4
title: D3D11_FEATURE_DATA_D3D11_OPTIONS4 (d3d11_4.h)
description: Describes Direct3D 11.4 feature options in the current graphics driver.
helpviewer_keywords: ["D3D11_FEATURE_DATA_D3D11_OPTIONS4","D3D11_FEATURE_DATA_D3D11_OPTIONS4 structure [Direct3D 11]","d3d11_4/D3D11_FEATURE_DATA_D3D11_OPTIONS4","direct3d11.d3d11_feature_data_d3d11_options4"]
old-location: direct3d11\d3d11_feature_data_d3d11_options4.htm
tech.root: direct3d11
ms.assetid: BC0DD66C-3452-440D-87EA-1504EFF89E3F
ms.date: 12/05/2018
ms.keywords: D3D11_FEATURE_DATA_D3D11_OPTIONS4, D3D11_FEATURE_DATA_D3D11_OPTIONS4 structure [Direct3D 11], d3d11_4/D3D11_FEATURE_DATA_D3D11_OPTIONS4, direct3d11.d3d11_feature_data_d3d11_options4
req.header: d3d11_4.h
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
req.typenames: D3D11_FEATURE_DATA_D3D11_OPTIONS4
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_FEATURE_DATA_D3D11_OPTIONS4
 - d3d11_4/D3D11_FEATURE_DATA_D3D11_OPTIONS4
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11_4.h
api_name:
 - D3D11_FEATURE_DATA_D3D11_OPTIONS4
---

# D3D11_FEATURE_DATA_D3D11_OPTIONS4 structure


## -description

Describes Direct3D 11.4 feature options in the current graphics driver.

## -struct-fields

### -field ExtendedNV12SharedTextureSupported

Specifies a BOOL that determines if NV12 textures can be shared across processes and D3D devices.

## -remarks

Use this structure with the D3D11_FEATURE_D3D11_OPTIONS4 member of <a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature">D3D11_FEATURE</a>. 

Refer to the section on NV12 in <a href="/windows/desktop/direct3d11/direct3d-11-4-features">Direct3D 11.4 Features</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-structures">Core Structures</a>