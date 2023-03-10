---
UID: NS:d3d11.D3D11_AUTHENTICATED_PROTECTION_FLAGS
title: D3D11_AUTHENTICATED_PROTECTION_FLAGS
description: Specifies the protection level for video content.
tech.root: direct3d11
helpviewer_keywords: ["D3D11_AUTHENTICATED_PROTECTION_FLAGS"]
ms.assetid: 037AB541-2E68-460C-8626-7F22C6C3E425
ms.date: 05/13/2019
ms.keywords: D3D11_AUTHENTICATED_PROTECTION_FLAGS
targetos: Windows
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: d3d11.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.typenames: D3D11_AUTHENTICATED_PROTECTION_FLAGS
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - D3D11_AUTHENTICATED_PROTECTION_FLAGS
 - d3d11/D3D11_AUTHENTICATED_PROTECTION_FLAGS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d11.h
api_name:
 - D3D11_AUTHENTICATED_PROTECTION_FLAGS
---

# D3D11_AUTHENTICATED_PROTECTION_FLAGS


## -description

Specifies the protection level for video content.

## -struct-fields

### -field Flags

### -field ProtectionEnabled

If 1, video content protection is enabled.

### -field OverlayOrFullscreenRequired

If 1, the application requires video to be displayed using either a hardware overlay or full-screen exclusive mode.

### -field Reserved

Reserved. Set all bits to zero.

### -field __MIDL___MIDL_itf_d3d11_0000_0034_0001

### -field Value

Use this member to access all of the bits in the union.

## -remarks

## -see-also

<a href="/windows/desktop/medfound/direct3d-11-video-structures">Direct3D 11 Video Structures</a>