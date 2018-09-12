---
UID: NL:gdipluseffects.Effect
title: Effect
author: windows-sdk-content
description: The Effect class serves as a base class for eleven classes that you can use to apply effects and adjustments to bitmaps. The following classes descend from Effect.
old-location: gdiplus\_gdiplus_CLASS_Effect_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\effect.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
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
<a href="https://msdn.microsoft.com/a061b15b-bce4-4b38-adba-836b6b295c80">Blur</a>
</li>
<li>
<a href="https://msdn.microsoft.com/28d30f3d-5e55-4d65-bbc2-6fa2e049f349">Sharpen</a>
</li>
<li>
<a href="https://msdn.microsoft.com/f012ec61-986d-40f4-a730-1b73a52952a8">Tint</a>
</li>
<li>
<a href="https://msdn.microsoft.com/6eb81857-758d-4302-a5e7-4f8b40025b03">RedEyeCorrection</a>
</li>
<li>
<a href="https://msdn.microsoft.com/99a4a671-e128-4a1b-8c8a-e9231bd44e96">ColorMatrixEffect</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d13dc185-e6f2-4a0f-b972-e9b6ce0859c6">ColorLUT</a>
</li>
<li>
<a href="https://msdn.microsoft.com/92eaf786-ab9e-46ae-af02-e620b3a35a8a">BrightnessContrast</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3bb652eb-62f0-4948-9484-4439dc9bd54e">HueSaturationLightness</a>
</li>
<li>
<a href="https://msdn.microsoft.com/87366bae-a67a-46bd-b06c-2c80b80ab800">ColorBalance</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0256fa03-f029-472e-988a-9eb7ed117673">Levels</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1ea62f08-f591-4da5-8fcc-74df7ddcebe4">ColorCurve</a>
</li>
</ul>To apply and effect to a bitmap, create an instance of one of the descendants of the Effect class, and pass the address of that descendant to the <a href="https://msdn.microsoft.com/cb85a7ac-5af0-45c7-8035-d7bc2827af6a">Graphics::DrawImage</a> method or to the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method.

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
<a href="https://msdn.microsoft.com/fef56d3b-e633-4468-a686-18242da6d29c">Effect::Effect</a>
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
<a href="https://msdn.microsoft.com/b418496f-4304-4885-bcba-c8178b90a788">Effect::GetAuxData</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b418496f-4304-4885-bcba-c8178b90a788">Effect::GetAuxData</a> gets a pointer to a set of lookup tables created by a previous call to the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c19c3891-2894-4655-b5c8-1306bfb72244">Effect::GetAuxDataSize</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/c19c3891-2894-4655-b5c8-1306bfb72244">Effect::GetAuxDataSize</a> method gets the size, in bytes, of the auxiliary data created by a previous call to the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41498160-cae7-4379-9151-f595ce158809">Effect::GetParameterSize</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/41498160-cae7-4379-9151-f595ce158809">Effect::GetParameterSize</a> method  gets the total size, in bytes, of the parameters currently set for this <b>Effect</b>. The <b>Effect::GetParameterSize</b> method is usually called on an object that is an instance of a descendant of the <b>Effect</b> class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9644e8d-a5d3-47ac-bd6a-6c720ef714f5">Effect::UseAuxData</a>
</td>
<td align="left" width="63%">
The <a href="https://msdn.microsoft.com/b9644e8d-a5d3-47ac-bd6a-6c720ef714f5">Effect::UseAuxData</a> method sets or clears a flag that specifies whether the <a href="https://msdn.microsoft.com/6b3d0a2f-acff-47a7-bc9f-6e9d659f683c">Bitmap::ApplyEffect</a> method should return a pointer to the auxiliary data that it creates. 

</td>
</tr>
</table> 

