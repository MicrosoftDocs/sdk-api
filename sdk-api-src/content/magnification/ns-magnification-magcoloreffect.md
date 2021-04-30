---
UID: NS:magnification.tagMAGCOLOREFFECT
title: MAGCOLOREFFECT (magnification.h)
description: Describes a color transformation matrix that a magnifier control uses to apply a color effect to magnified screen content.
helpviewer_keywords: ["*PMAGCOLOREFFECT","MAGCOLOREFFECT","MAGCOLOREFFECT structure [Magnification API]","PMAGCOLOREFFECT","PMAGCOLOREFFECT structure pointer [Magnification API]","magapi.magapi_magcoloreffect","magapi_magcoloreffect","magnification/MAGCOLOREFFECT","magnification/PMAGCOLOREFFECT"]
old-location: magapi\magapi_magcoloreffect.htm
tech.root: magapi
ms.assetid: VS|magapi|~\magapi\reference\structures\magcoloreffectstruct.htm
ms.date: 12/05/2018
ms.keywords: '*PMAGCOLOREFFECT, MAGCOLOREFFECT, MAGCOLOREFFECT structure [Magnification API], PMAGCOLOREFFECT, PMAGCOLOREFFECT structure pointer [Magnification API], magapi.magapi_magcoloreffect, magapi_magcoloreffect, magnification/MAGCOLOREFFECT, magnification/PMAGCOLOREFFECT'
req.header: magnification.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MAGCOLOREFFECT, *PMAGCOLOREFFECT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMAGCOLOREFFECT
 - magnification/tagMAGCOLOREFFECT
 - PMAGCOLOREFFECT
 - magnification/PMAGCOLOREFFECT
 - MAGCOLOREFFECT
 - magnification/MAGCOLOREFFECT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Magnification.h
api_name:
 - MAGCOLOREFFECT
---

## -description

Describes a color transformation matrix that a magnifier control uses to apply a color effect to magnified screen content.

## -struct-fields

### -field transform

Type: <b>float [5] [5]</b>

The color transformation matrix.

## -remarks

The values in the matrix are for red, blue, green, alpha, and color translation. For more information, see 
<a href="/windows/desktop/gdiplus/-gdiplus-using-a-color-matrix-to-transform-a-single-color-use">Using a Color Matrix to Transform a Single Color</a> in the Windows GDI+ documentation.

## -see-also

<a href="/previous-versions/windows/desktop/api/magnification/nf-magnification-maggetcoloreffect">MagGetColorEffect</a>

<a href="/previous-versions/windows/desktop/api/magnification/nf-magnification-magsetcoloreffect">MagSetColorEffect</a>
