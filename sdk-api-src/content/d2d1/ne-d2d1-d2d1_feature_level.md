---
UID: NE:d2d1.D2D1_FEATURE_LEVEL
title: D2D1_FEATURE_LEVEL (d2d1.h)
description: Describes the minimum DirectX support required for hardware rendering by a render target.
helpviewer_keywords: ["D2D1_FEATURE_LEVEL","D2D1_FEATURE_LEVEL enumeration [Direct2D]","D2D1_FEATURE_LEVEL_10","D2D1_FEATURE_LEVEL_9","D2D1_FEATURE_LEVEL_DEFAULT","d2d1/D2D1_FEATURE_LEVEL","d2d1/D2D1_FEATURE_LEVEL_10","d2d1/D2D1_FEATURE_LEVEL_9","d2d1/D2D1_FEATURE_LEVEL_DEFAULT","direct2d.D2D1_FEATURE_LEVEL"]
old-location: direct2d\D2D1_FEATURE_LEVEL.htm
tech.root: Direct2D
ms.assetid: d9604c37-7345-40e3-850c-2e2c99353ba5
ms.date: 12/05/2018
ms.keywords: D2D1_FEATURE_LEVEL, D2D1_FEATURE_LEVEL enumeration [Direct2D], D2D1_FEATURE_LEVEL_10, D2D1_FEATURE_LEVEL_9, D2D1_FEATURE_LEVEL_DEFAULT, d2d1/D2D1_FEATURE_LEVEL, d2d1/D2D1_FEATURE_LEVEL_10, d2d1/D2D1_FEATURE_LEVEL_9, d2d1/D2D1_FEATURE_LEVEL_DEFAULT, direct2d.D2D1_FEATURE_LEVEL
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
req.typenames: D2D1_FEATURE_LEVEL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_FEATURE_LEVEL
 - d2d1/D2D1_FEATURE_LEVEL
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
 - D2D1_FEATURE_LEVEL
---

# D2D1_FEATURE_LEVEL enumeration


## -description

Describes the minimum DirectX support required for hardware rendering by a render target.

## -enum-fields

### -field D2D1_FEATURE_LEVEL_DEFAULT:0

Direct2D determines whether the video card provides adequate hardware rendering support.

### -field D2D1_FEATURE_LEVEL_9

The video card must support DirectX 9.

### -field D2D1_FEATURE_LEVEL_10

The video card must support DirectX 10.

### -field D2D1_FEATURE_LEVEL_FORCE_DWORD:0xffffffff

## -see-also

<a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_render_target_properties">D2D1_RENDER_TARGET_PROPERTIES</a>

