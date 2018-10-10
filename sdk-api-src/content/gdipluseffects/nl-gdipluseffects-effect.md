---
UID: NL:gdipluseffects.Effect
title: Effect
author: windows-sdk-content
description: The Effect class serves as a base class for eleven classes that you can use to apply effects and adjustments to bitmaps. The following classes descend from Effect.
old-location: gdiplus\_gdiplus_CLASS_Effect_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\effect.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Effect, Effect class [GDI+], Effect class [GDI+],described, _gdiplus_CLASS_Effect_Class, gdiplus._gdiplus_CLASS_Effect_Class, gdipluseffects/Effect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
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
---

# Effect class


## -description


The <b>Effect</b> class serves as a base class for eleven classes that you can use to apply effects and adjustments to bitmaps. The following classes descend from <b>Effect</b>.
<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms534422(v=VS.85).aspx">Blur</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms534503(v=VS.85).aspx">Sharpen</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms534513(v=VS.85).aspx">Tint</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms534499(v=VS.85).aspx">RedEyeCorrection</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms534431(v=VS.85).aspx">ColorMatrixEffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms534430(v=VS.85).aspx">ColorLUT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms534423(v=VS.85).aspx">BrightnessContrast</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms534461(v=VS.85).aspx">HueSaturationLightness</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms534428(v=VS.85).aspx">ColorBalance</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms534471(v=VS.85).aspx">Levels</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/ms534429(v=VS.85).aspx">ColorCurve</a>
</li>
</ul>To apply and effect to a bitmap, create an instance of one of the descendants of the Effect class, and pass the address of that descendant to the <a href="https://msdn.microsoft.com/en-us/library/ms536058(v=VS.85).aspx">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/en-us/library/ms536284(v=VS.85).aspx">Bitmap::ApplyEffect</a> method.

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
<a href="https://msdn.microsoft.com/en-us/library/ms536214(v=VS.85).aspx">Effect::Effect</a>
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
<a href="https://msdn.microsoft.com/en-us/library/ms536210(v=VS.85).aspx">Effect::GetAuxData</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms536210(v=VS.85).aspx">Effect::GetAuxData</a> gets a pointer to a set of lookup tables created by a previous call to the <a href="https://msdn.microsoft.com/en-us/library/ms536284(v=VS.85).aspx">Bitmap::ApplyEffect</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536211(v=VS.85).aspx">Effect::GetAuxDataSize</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms536211(v=VS.85).aspx">Effect::GetAuxDataSize</a> method gets the size, in bytes, of the auxiliary data created by a previous call to the <a href="https://msdn.microsoft.com/en-us/library/ms536284(v=VS.85).aspx">Bitmap::ApplyEffect</a> method. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536212(v=VS.85).aspx">Effect::GetParameterSize</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms536212(v=VS.85).aspx">Effect::GetParameterSize</a> method  gets the total size, in bytes, of the parameters currently set for this <b>Effect</b>. The <b>Effect::GetParameterSize</b> method is usually called on an object that is an instance of a descendant of the <b>Effect</b> class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms536213(v=VS.85).aspx">Effect::UseAuxData</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/en-us/library/ms536213(v=VS.85).aspx">Effect::UseAuxData</a> method sets or clears a flag that specifies whether the <a href="https://msdn.microsoft.com/en-us/library/ms536284(v=VS.85).aspx">Bitmap::ApplyEffect</a> method should return a pointer to the auxiliary data that it creates. 

</td>
</tr>
</table> 

