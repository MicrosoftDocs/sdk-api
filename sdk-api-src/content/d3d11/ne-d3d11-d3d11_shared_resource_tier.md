---
UID: NE:d3d11.D3D11_SHARED_RESOURCE_TIER
title: D3D11_SHARED_RESOURCE_TIER
description: Defines constants that specify the level of support for shared resources in the current graphics driver
tech.root: direct3d11
ms.date: 07/28/2022
helpviewer_keywords: ["D3D11_SHARED_RESOURCE_TIER"]
ms.keywords: D3D11_SHARED_RESOURCE_TIER
targetos: Windows
req.construct-type: enumeration
req.ddi-compliance: 
req.header: d3d11.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: 
req.umdf-ver: 
f1_keywords:
 - D3D11_SHARED_RESOURCE_TIER
 - d3d11/D3D11_SHARED_RESOURCE_TIER
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_SHARED_RESOURCE_TIER
---

## -description

Defines constants that specify the level of support for shared resources in the current graphics driver.

## -enum-fields

### -field D3D11_SHARED_RESOURCE_TIER_0:0

Specifies the support available when [D3D11_FEATURE_DATA_D3D11_OPTIONS::ExtendedResourceSharing](./ns-d3d11-d3d11_feature_data_d3d11_options.md) is `FALSE` (only very old drivers have this value set to `FALSE`).

See [Extended support for shared Texture2D resources](/windows/win32/direct3d11/direct3d-11-1-features#extended-support-for-shared-texture2d-resources).

### -field D3D11_SHARED_RESOURCE_TIER_1

Specifies the support available when [D3D11_FEATURE_DATA_D3D11_OPTIONS::ExtendedResourceSharing](./ns-d3d11-d3d11_feature_data_d3d11_options.md) and [D3D11_FEATURE_DATA_D3D11_OPTIONS4::ExtendedNV12SharedTextureSupported](/windows/win32/api/d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4) are `TRUE`.

You can share additional formats; see [Extended support for shared Texture2D resources](/windows/win32/direct3d11/direct3d-11-1-features#extended-support-for-shared-texture2d-resources).

Only formats that are still shareable when **D3D11_FEATURE_DATA_D3D11_OPTIONS::ExtendedResourceSharing** == `FALSE` can be shared across APIs between Direct3D 11 and Direct3D 12.

Resource formats added by **D3D11_FEATURE_DATA_D3D11_OPTIONS::ExtendedResourceSharing** == `TRUE` can't be shared across APIs.

### -field D3D11_SHARED_RESOURCE_TIER_2

Specifies the support available when [D3D11_FEATURE_DATA_D3D11_OPTIONS4::ExtendedNV12SharedTextureSupported](../d3d11_4/ns-d3d11_4-d3d11_feature_data_d3d11_options4.md) is `TRUE`. Also see [Extended NV12 texture support](/windows/win32/direct3d11/direct3d-11-4-features#extended-nv12-texture-support).

See [Extended support for shared Texture2D resources](/windows/win32/direct3d11/direct3d-11-1-features#extended-support-for-shared-texture2d-resources).

Sharing across APIs between Direct3D 11 and Direct3D 12 is possible for the **D3D11_FEATURE_DATA_D3D11_OPTIONS::ExtendedResourceSharing** == `TRUE` format list.

### -field D3D11_SHARED_RESOURCE_TIER_3

Specifies that [DXGI_FORMAT_R11G11B10_FLOAT](../dxgiformat/ne-dxgiformat-dxgi_format.md) supports NT handle sharing. Also see [CreateSharedHandle](../dxgi1_2/nf-dxgi1_2-idxgiresource1-createsharedhandle.md).

Sharing across APIs between Direct3D 11 and Direct3D 12 is possible for the **DXGI_FORMAT_R11G11B10_FLOAT** format.

## -remarks

## -see-also

* [Extended support for shared Texture2D resources](/windows/win32/direct3d11/direct3d-11-1-features#extended-support-for-shared-texture2d-resources)
