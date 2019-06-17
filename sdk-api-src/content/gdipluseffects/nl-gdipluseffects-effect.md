---
UID: NL:gdipluseffects.Effect
title: Effect (gdipluseffects.h)
author: windows-sdk-content
description: The Effect class serves as a base class for eleven classes that you can use to apply effects and adjustments to bitmaps. The following classes descend from Effect.
old-location: gdiplus\_gdiplus_CLASS_Effect_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\effect.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Effect, Effect class [GDI+], Effect class [GDI+],described, _gdiplus_CLASS_Effect_Class, gdiplus._gdiplus_CLASS_Effect_Class, gdipluseffects/Effect
ms.topic: class
f1_keywords: ["gdipluseffects/Effect"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdipluseffects.h
api_name:
 - Effect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# Effect class


## -description


The <b>Effect</b> class serves as a base class for eleven classes that you can use to apply effects and adjustments to bitmaps. The following classes descend from <b>Effect</b>.
<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nl-gdipluseffects-blur">Blur</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nl-gdipluseffects-sharpen">Sharpen</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nl-gdipluseffects-tint">Tint</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nl-gdipluseffects-redeyecorrection">RedEyeCorrection</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nl-gdipluseffects-colormatrixeffect">ColorMatrixEffect</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nl-gdipluseffects-colorlut">ColorLUT</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nl-gdipluseffects-brightnesscontrast">BrightnessContrast</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nl-gdipluseffects-huesaturationlightness">HueSaturationLightness</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nl-gdipluseffects-colorbalance">ColorBalance</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nl-gdipluseffects-levels">Levels</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nl-gdipluseffects-colorcurve">ColorCurve</a>
</li>
</ul>To apply and effect to a bitmap, create an instance of one of the descendants of the Effect class, and pass the address of that descendant to the <a href="https://docs.microsoft.com/previous-versions//ms536058(v=vs.85)">Graphics::DrawImage</a> method or to the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">Effect</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Constructors</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="constructors"></a>Constructors</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">Effect</b> class has these constructors.
<table class="members" id="memberListConstructors">
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nf-gdipluseffects-effect-effect">Effect::Effect</a>
</td>
<td align="left" width="63%">
Creates an <b>Effect</b> object. 

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>Effect</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nf-gdipluseffects-effect-getauxdata">Effect::GetAuxData</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nf-gdipluseffects-effect-getauxdata">Effect::GetAuxData</a> gets a pointer to a set of lookup tables created by a previous call to the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nf-gdipluseffects-effect-getauxdatasize">Effect::GetAuxDataSize</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nf-gdipluseffects-effect-getauxdatasize">Effect::GetAuxDataSize</a> method gets the size, in bytes, of the auxiliary data created by a previous call to the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nf-gdipluseffects-effect-getparametersize">Effect::GetParameterSize</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nf-gdipluseffects-effect-getparametersize">Effect::GetParameterSize</a> method  gets the total size, in bytes, of the parameters currently set for this <b>Effect</b>. The <b>Effect::GetParameterSize</b> method is usually called on an object that is an instance of a descendant of the <b>Effect</b> class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nf-gdipluseffects-effect-useauxdata">Effect::UseAuxData</a>
</td>
<td align="left" width="63%">
The <a href="https://docs.microsoft.com/windows/desktop/api/gdipluseffects/nf-gdipluseffects-effect-useauxdata">Effect::UseAuxData</a> method sets or clears a flag that specifies whether the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-bitmap-applyeffect(inbitmap_inint_ineffect_inrect_outrect_outbitmap)">Bitmap::ApplyEffect</a> method should return a pointer to the auxiliary data that it creates. 

</td>
</tr>
</table> 

