---
UID: NE:d2d1effects.D2D1_DPICOMPENSATION_PROP
title: D2D1_DPICOMPENSATION_PROP (d2d1effects.h)
author: windows-sdk-content
description: Identifiers for properties of the DPI compensation effect.
old-location: direct2d\d2d1_dpicompensation_prop.htm
tech.root: Direct2D
ms.assetid: B8956D69-B014-49EA-BCBA-5AE9DC051A5A
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D2D1_DPICOMPENSATION_PROP, D2D1_DPICOMPENSATION_PROP enumeration [Direct2D], D2D1_DPICOMPENSATION_PROP_BORDER_MODE, D2D1_DPICOMPENSATION_PROP_INPUT_DPI, D2D1_DPICOMPENSATION_PROP_INTERPOLATION_MODE, d2d1effects/D2D1_DPICOMPENSATION_PROP, d2d1effects/D2D1_DPICOMPENSATION_PROP_BORDER_MODE, d2d1effects/D2D1_DPICOMPENSATION_PROP_INPUT_DPI, d2d1effects/D2D1_DPICOMPENSATION_PROP_INTERPOLATION_MODE, direct2d.d2d1_dpicompensation_prop
ms.topic: enum
f1_keywords: 
 - "d2d1effects/D2D1_DPICOMPENSATION_PROP"
req.header: d2d1effects.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effects.h
api_name:
 - D2D1_DPICOMPENSATION_PROP
targetos: Windows
req.typenames: D2D1_DPICOMPENSATION_PROP
req.redist: 
ms.custom: 19H1
---

# D2D1_DPICOMPENSATION_PROP enumeration


## -description


Identifiers for properties of the <a href="https://docs.microsoft.com/windows/desktop/Direct2D/dpi-compensation">DPI compensation effect</a>.
        


## -enum-fields




### -field D2D1_DPICOMPENSATION_PROP_INTERPOLATION_MODE

The interpolation mode the effect uses to scale the image.
            

The type is <a href="https://docs.microsoft.com/windows/desktop/api/d2d1effects/ne-d2d1effects-d2d1_dpicompensation_interpolation_mode">D2D1_DPICOMPENSATION_INTERPOLATION_MODE</a>.

The default value is D2D1_DPICOMPENSATION_INTERPOLATION_MODE_LINEAR.


### -field D2D1_DPICOMPENSATION_PROP_BORDER_MODE

The mode used to calculate the border of the image, soft or hard. See Border modes for more info.
            

The type is <a href="https://docs.microsoft.com/windows/desktop/api/d2d1effects/ne-d2d1effects-d2d1_border_mode">D2D1_BORDER_MODE</a>.

The default value is D2D1_BORDER_MODE_SOFT.


### -field D2D1_DPICOMPENSATION_PROP_INPUT_DPI

The DPI of the input image.
            

The type is FLOAT.

The default value is 96.0f.


### -field D2D1_DPICOMPENSATION_PROP_FORCE_DWORD



