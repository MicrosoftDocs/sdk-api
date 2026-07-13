---
UID: NL:gdipluseffects.Effect
title: Effect (gdipluseffects.h)
description: The Effect class serves as a base class for eleven classes that you can use to apply effects and adjustments to bitmaps. The following classes descend from Effect.
helpviewer_keywords: ["Effect","Effect class [GDI+]","Effect class [GDI+]","described","_gdiplus_CLASS_Effect_Class","gdiplus._gdiplus_CLASS_Effect_Class","gdipluseffects/Effect"]
old-location: gdiplus\_gdiplus_CLASS_Effect_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\effect.htm
ms.date: 12/05/2018
ms.keywords: Effect, Effect class [GDI+], Effect class [GDI+],described, _gdiplus_CLASS_Effect_Class, gdiplus._gdiplus_CLASS_Effect_Class, gdipluseffects/Effect
req.header: gdipluseffects.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Effect
 - gdipluseffects/Effect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdipluseffects.h
api_name:
 - Effect
---

# Effect class


## -description

The <b>Effect</b> class serves as a base class for eleven classes that you can use to apply effects and adjustments to bitmaps. The following classes descend from <b>Effect</b>.
<ul>
<li>
<a href="/windows/win32/api/gdipluseffects/nl-gdipluseffects-blur">Blur</a>
</li>
<li>
<a href="/windows/win32/api/gdipluseffects/nl-gdipluseffects-sharpen">Sharpen</a>
</li>
<li>
<a href="/windows/win32/api/gdipluseffects/nl-gdipluseffects-tint">Tint</a>
</li>
<li>
<a href="/windows/win32/api/gdipluseffects/nl-gdipluseffects-redeyecorrection">RedEyeCorrection</a>
</li>
<li>
<a href="/windows/win32/api/gdipluseffects/nl-gdipluseffects-colormatrixeffect">ColorMatrixEffect</a>
</li>
<li>
<a href="/windows/win32/api/gdipluseffects/nl-gdipluseffects-colorlut">ColorLUT</a>
</li>
<li>
<a href="/windows/win32/api/gdipluseffects/nl-gdipluseffects-brightnesscontrast">BrightnessContrast</a>
</li>
<li>
<a href="/windows/win32/api/gdipluseffects/nl-gdipluseffects-huesaturationlightness">HueSaturationLightness</a>
</li>
<li>
<a href="/windows/win32/api/gdipluseffects/nl-gdipluseffects-colorbalance">ColorBalance</a>
</li>
<li>
<a href="/windows/win32/api/gdipluseffects/nl-gdipluseffects-levels">Levels</a>
</li>
<li>
<a href="/windows/win32/api/gdipluseffects/nl-gdipluseffects-colorcurve">ColorCurve</a>
</li>
</ul>To apply and effect to a bitmap, create an instance of one of the descendants of the Effect class, and pass the address of that descendant to the <a href="/previous-versions/ms536058(v=vs.85)">Graphics::DrawImage</a> method or to the <a href="/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method.

