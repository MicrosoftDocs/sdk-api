---
UID: NS:d3d11.D3D11_FEATURE_DATA_D3D9_OPTIONS
title: D3D11_FEATURE_DATA_D3D9_OPTIONS (d3d11.h)
description: Describes Direct3D 9 feature options in the current graphics driver. (D3D11_FEATURE_DATA_D3D9_OPTIONS)
helpviewer_keywords: ["D3D11_FEATURE_DATA_D3D9_OPTIONS","D3D11_FEATURE_DATA_D3D9_OPTIONS structure [Direct3D 11]","d3d11/D3D11_FEATURE_DATA_D3D9_OPTIONS","direct3d11.d3d11_feature_data_d3d9_options"]
old-location: direct3d11\d3d11_feature_data_d3d9_options.htm
tech.root: direct3d11
ms.assetid: E5262261-28D7-4F7A-AB9A-A73FEADAE8FD
ms.date: 12/05/2018
ms.keywords: D3D11_FEATURE_DATA_D3D9_OPTIONS, D3D11_FEATURE_DATA_D3D9_OPTIONS structure [Direct3D 11], d3d11/D3D11_FEATURE_DATA_D3D9_OPTIONS, direct3d11.d3d11_feature_data_d3d9_options
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: D3D11_FEATURE_DATA_D3D9_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_FEATURE_DATA_D3D9_OPTIONS
 - d3d11/D3D11_FEATURE_DATA_D3D9_OPTIONS
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
 - D3D11_FEATURE_DATA_D3D9_OPTIONS
---

# D3D11_FEATURE_DATA_D3D9_OPTIONS structure


## -description

<div class="alert"><b>Note</b>  This structure is supported by the Direct3D 11.1 runtime, which is available on Windows 8 and later operating systems.</div><div> </div>Describes Direct3D 9 feature options in the current graphics driver.

## -struct-fields

### -field FullNonPow2TextureSupport

Specifies whether the driver supports the nonpowers-of-2-unconditionally feature. For more information about this feature, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro">feature level</a>. The runtime sets this member to <b>TRUE</b> for hardware at Direct3D 10 and higher feature levels.  For hardware at Direct3D 9.3 and lower feature levels, the runtime sets this member to <b>FALSE</b> if the hardware and driver support the powers-of-2 (2D textures must have widths and heights specified as powers of two) feature or the nonpowers-of-2-conditionally feature. For more information about this feature, see feature level.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-structures">Core Structures</a>



<a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature">D3D11_FEATURE</a>
