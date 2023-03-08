---
UID: NE:d2d1.D2D1_RENDER_TARGET_TYPE
title: D2D1_RENDER_TARGET_TYPE (d2d1.h)
description: Describes whether a render target uses hardware or software rendering, or if Direct2D should select the rendering mode.
helpviewer_keywords: ["D2D1_RENDER_TARGET_TYPE","D2D1_RENDER_TARGET_TYPE enumeration [Direct2D]","D2D1_RENDER_TARGET_TYPE_DEFAULT","D2D1_RENDER_TARGET_TYPE_HARDWARE","D2D1_RENDER_TARGET_TYPE_SOFTWARE","d2d1/D2D1_RENDER_TARGET_TYPE","d2d1/D2D1_RENDER_TARGET_TYPE_DEFAULT","d2d1/D2D1_RENDER_TARGET_TYPE_HARDWARE","d2d1/D2D1_RENDER_TARGET_TYPE_SOFTWARE","direct2d.D2D1_RENDER_TARGET_TYPE"]
old-location: direct2d\D2D1_RENDER_TARGET_TYPE.htm
tech.root: Direct2D
ms.assetid: 4ae6e4cf-e1c9-476e-a7b5-31cdad9cf321
ms.date: 12/05/2018
ms.keywords: D2D1_RENDER_TARGET_TYPE, D2D1_RENDER_TARGET_TYPE enumeration [Direct2D], D2D1_RENDER_TARGET_TYPE_DEFAULT, D2D1_RENDER_TARGET_TYPE_HARDWARE, D2D1_RENDER_TARGET_TYPE_SOFTWARE, d2d1/D2D1_RENDER_TARGET_TYPE, d2d1/D2D1_RENDER_TARGET_TYPE_DEFAULT, d2d1/D2D1_RENDER_TARGET_TYPE_HARDWARE, d2d1/D2D1_RENDER_TARGET_TYPE_SOFTWARE, direct2d.D2D1_RENDER_TARGET_TYPE
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
req.typenames: D2D1_RENDER_TARGET_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_RENDER_TARGET_TYPE
 - d2d1/D2D1_RENDER_TARGET_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1.h
api_name:
 - D2D1_RENDER_TARGET_TYPE
---

# D2D1_RENDER_TARGET_TYPE enumeration


## -description

Describes whether a render target uses hardware or software rendering, or if Direct2D should select the rendering mode.

## -enum-fields

### -field D2D1_RENDER_TARGET_TYPE_DEFAULT:0

The render target uses hardware rendering, if available; otherwise, it uses software rendering.

### -field D2D1_RENDER_TARGET_TYPE_SOFTWARE:1

The render target uses software rendering only.

### -field D2D1_RENDER_TARGET_TYPE_HARDWARE:2

The render target uses hardware rendering only.

### -field D2D1_RENDER_TARGET_TYPE_FORCE_DWORD:0xffffffff

## -remarks

Not every render target supports hardware rendering. For more information, see the <a href="/windows/win32/Direct2D/render-targets-overview">Render Targets Overview</a>.

## -see-also

<a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_render_target_properties">D2D1_RENDER_TARGET_PROPERTIES</a>



<a href="/windows/win32/Direct2D/render-targets-overview">Render Targets Overview</a>

