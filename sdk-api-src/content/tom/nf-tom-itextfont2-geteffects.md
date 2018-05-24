---
UID: NF:tom.ITextFont2.GetEffects
title: ITextFont2::GetEffects
author: windows-driver-content
description: Gets the character format effects.
old-location: controls\itextfont2_geteffects.htm
old-project: Controls
ms.assetid: a182df7e-2024-48fc-9767-7110ffff0b4c
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetEffects, GetEffects method [Windows Controls], GetEffects method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetEffects method, ITextFont2.GetEffects, ITextFont2::GetEffects, controls.itextfont2_geteffects, tom/ITextFont2::GetEffects, tomAllCaps, tomBold, tomDisabled, tomEmboss, tomHidden, tomImprint, tomInlineObjectStart, tomItalic, tomLink, tomLinkProtected, tomMathZone, tomMathZoneDisplay, tomMathZoneNoBuildUp, tomMathZoneOrdinary, tomOutline, tomProtected, tomRevised, tomShadow, tomSmallCaps, tomStrikeout, tomUnderline
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MANCODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextFont2.GetEffects
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont2::GetEffects


## -description


Gets the character format effects.


## -parameters




### -param pValue [out]

Type: <b>long*</b>

A combination of the following character format values.

<a id="tomAllCaps"></a>
<a id="tomallcaps"></a>
<a id="TOMALLCAPS"></a>


#### tomAllCaps

<a id="tomBold"></a>
<a id="tombold"></a>
<a id="TOMBOLD"></a>


#### tomBold

<a id="tomDisabled"></a>
<a id="tomdisabled"></a>
<a id="TOMDISABLED"></a>


#### tomDisabled

<a id="tomEmboss"></a>
<a id="tomemboss"></a>
<a id="TOMEMBOSS"></a>


#### tomEmboss

<a id="tomHidden"></a>
<a id="tomhidden"></a>
<a id="TOMHIDDEN"></a>


#### tomHidden

<a id="tomImprint"></a>
<a id="tomimprint"></a>
<a id="TOMIMPRINT"></a>


#### tomImprint

<a id="tomInlineObjectStart"></a>
<a id="tominlineobjectstart"></a>
<a id="TOMINLINEOBJECTSTART"></a>


#### tomInlineObjectStart

<a id="tomItalic"></a>
<a id="tomitalic"></a>
<a id="TOMITALIC"></a>


#### tomItalic

<a id="tomLink"></a>
<a id="tomlink"></a>
<a id="TOMLINK"></a>


#### tomLink

<a id="tomLinkProtected"></a>
<a id="tomlinkprotected"></a>
<a id="TOMLINKPROTECTED"></a>


#### tomLinkProtected

<a id="tomMathZone"></a>
<a id="tommathzone"></a>
<a id="TOMMATHZONE"></a>


#### tomMathZone

<a id="tomMathZoneDisplay"></a>
<a id="tommathzonedisplay"></a>
<a id="TOMMATHZONEDISPLAY"></a>


#### tomMathZoneDisplay

<a id="tomMathZoneNoBuildUp"></a>
<a id="tommathzonenobuildup"></a>
<a id="TOMMATHZONENOBUILDUP"></a>


#### tomMathZoneNoBuildUp

<a id="tomMathZoneOrdinary"></a>
<a id="tommathzoneordinary"></a>
<a id="TOMMATHZONEORDINARY"></a>


#### tomMathZoneOrdinary

<a id="tomOutline"></a>
<a id="tomoutline"></a>
<a id="TOMOUTLINE"></a>


#### tomOutline

<a id="tomProtected"></a>
<a id="tomprotected"></a>
<a id="TOMPROTECTED"></a>


#### tomProtected

<a id="tomRevised"></a>
<a id="tomrevised"></a>
<a id="TOMREVISED"></a>


#### tomRevised

<a id="tomShadow"></a>
<a id="tomshadow"></a>
<a id="TOMSHADOW"></a>


#### tomShadow

<a id="tomSmallCaps"></a>
<a id="tomsmallcaps"></a>
<a id="TOMSMALLCAPS"></a>


#### tomSmallCaps

<a id="tomStrikeout"></a>
<a id="tomstrikeout"></a>
<a id="TOMSTRIKEOUT"></a>


#### tomStrikeout

<a id="tomUnderline"></a>
<a id="tomunderline"></a>
<a id="TOMUNDERLINE"></a>


#### tomUnderline

If the  <a href="tomconstants.htm">tomInlineObjectStart</a> flag is set, you might want to call <a href="https://msdn.microsoft.com/0d86f2a4-d046-4d27-b128-40f2a3dd359a">GetInlineObject</a> for more inline object properties.



### -param pMask [out]

Type: <b>long*</b>

The differences in these flags over the range. A value of zero indicates that the properties are the same over the range. For an insertion point, this value is always zero.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/edfc882e-6f76-498f-ae3f-4978ea728d1b">ITextFont2::SetEffects</a>
 

 

