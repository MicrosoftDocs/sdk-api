---
UID: NE:d2d1.D2D1_RENDER_TARGET_USAGE
title: D2D1_RENDER_TARGET_USAGE (d2d1.h)
description: Describes how a render target is remoted and whether it should be GDI-compatible. This enumeration allows a bitwise combination of its member values.
helpviewer_keywords: ["D2D1_RENDER_TARGET_USAGE","D2D1_RENDER_TARGET_USAGE enumeration [Direct2D]","D2D1_RENDER_TARGET_USAGE_FORCE_BITMAP_REMOTING","D2D1_RENDER_TARGET_USAGE_GDI_COMPATIBLE","D2D1_RENDER_TARGET_USAGE_NONE","d2d1/D2D1_RENDER_TARGET_USAGE","d2d1/D2D1_RENDER_TARGET_USAGE_FORCE_BITMAP_REMOTING","d2d1/D2D1_RENDER_TARGET_USAGE_GDI_COMPATIBLE","d2d1/D2D1_RENDER_TARGET_USAGE_NONE","direct2d.D2D1_RENDER_TARGET_USAGE"]
old-location: direct2d\D2D1_RENDER_TARGET_USAGE.htm
tech.root: Direct2D
ms.assetid: 12d717c4-5f81-4bbf-a693-042e51913081
ms.date: 12/05/2018
ms.keywords: D2D1_RENDER_TARGET_USAGE, D2D1_RENDER_TARGET_USAGE enumeration [Direct2D], D2D1_RENDER_TARGET_USAGE_FORCE_BITMAP_REMOTING, D2D1_RENDER_TARGET_USAGE_GDI_COMPATIBLE, D2D1_RENDER_TARGET_USAGE_NONE, d2d1/D2D1_RENDER_TARGET_USAGE, d2d1/D2D1_RENDER_TARGET_USAGE_FORCE_BITMAP_REMOTING, d2d1/D2D1_RENDER_TARGET_USAGE_GDI_COMPATIBLE, d2d1/D2D1_RENDER_TARGET_USAGE_NONE, direct2d.D2D1_RENDER_TARGET_USAGE
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
req.typenames: D2D1_RENDER_TARGET_USAGE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_RENDER_TARGET_USAGE
 - d2d1/D2D1_RENDER_TARGET_USAGE
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
 - D2D1_RENDER_TARGET_USAGE
---

# D2D1_RENDER_TARGET_USAGE enumeration


## -description

Describes how a render target is remoted and whether it should be GDI-compatible. This enumeration allows a bitwise combination of its member values.

## -enum-fields

### -field D2D1_RENDER_TARGET_USAGE_NONE:0x00000000

The render target attempts to use Direct3D command-stream remoting and uses bitmap remoting if stream remoting fails. The render target is not GDI-compatible.

### -field D2D1_RENDER_TARGET_USAGE_FORCE_BITMAP_REMOTING:0x00000001

The render target renders content locally and sends it to the terminal services client as a bitmap.

### -field D2D1_RENDER_TARGET_USAGE_GDI_COMPATIBLE:0x00000002

The render target can be used efficiently with GDI.

### -field D2D1_RENDER_TARGET_USAGE_FORCE_DWORD:0xffffffff

## -see-also

<a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_render_target_properties">D2D1_RENDER_TARGET_PROPERTIES</a>

