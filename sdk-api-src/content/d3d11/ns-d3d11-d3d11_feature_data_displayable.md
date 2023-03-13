---
UID: NS:d3d11.D3D11_FEATURE_DATA_DISPLAYABLE
title: D3D11_FEATURE_DATA_DISPLAYABLE
description: Describes the level of displayable surfaces supported in the current graphics driver.
ms.date: 07/01/2022
helpviewer_keywords:
 - D3D11_FEATURE_DATA_DISPLAYABLE
tech.root: direct3d11
req.construct-type: structure
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 11 (Build 10.0.22000.194)
req.target-min-winversvr: Windows 11 (Build 10.0.22000.194)
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
req.typenames: D3D11_FEATURE_DATA_DISPLAYABLE
req.redist: 
f1_keywords:
 - D3D11_FEATURE_DATA_DISPLAYABLE
 - d3d11/D3D11_FEATURE_DATA_DISPLAYABLE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_FEATURE_DATA_DISPLAYABLE
---

## -description

Describes the level of displayable surfaces supported in the current graphics driver. See [Displayable surfaces](/windows/win32/direct3d11/displayable-surfaces).

## -struct-fields

### -field DisplayableTexture

Type: **[BOOL](/windows/win32/winprog/windows-data-types)**

`true` if the driver supports displayable surfaces; otherwise, `false`.

### -field SharedResourceTier

Type: **[D3D11_SHARED_RESOURCE_TIER](/windows/win32/api/d3d11/ne-d3d11-d3d11_shared_resource_tier)**

The level of support for shared resources in the current graphics driver.

## -remarks

## -see-also

* [Displayable surfaces](/windows/win32/direct3d11/displayable-surfaces)
