---
UID: NF:tom.ITextFont2.GetEffects2
title: ITextFont2::GetEffects2
author: windows-sdk-content
description: Gets the additional character format effects.
old-location: controls\itextfont2_geteffects2.htm
old-project: controls
ms.assetid: 6b28c995-33dd-4f5b-ac89-eec367e0a4d5
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetEffects2, GetEffects2 method [Windows Controls], GetEffects2 method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetEffects2 method, ITextFont2.GetEffects2, ITextFont2::GetEffects2, controls.itextfont2_geteffects2, tom/ITextFont2::GetEffects2, tomAutoSpaceAlpha, tomAutoSpaceNumeric, tomAutoSpaceParens, tomDoublestrike, tomEmbeddedFont, tomModWidthPairs, tomModWidthSpace, tomOverlapping
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MANCODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextFont2.GetEffects2
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextFont2::GetEffects2


## -description


Gets the additional character format effects.


## -parameters




### -param pValue [out]

Type: <b>long*</b>

A combination of the following character format flags.

<a id="tomAutoSpaceAlpha"></a>
<a id="tomautospacealpha"></a>
<a id="TOMAUTOSPACEALPHA"></a>


#### tomAutoSpaceAlpha

<a id="tomAutoSpaceNumeric"></a>
<a id="tomautospacenumeric"></a>
<a id="TOMAUTOSPACENUMERIC"></a>


#### tomAutoSpaceNumeric

<a id="tomAutoSpaceParens"></a>
<a id="tomautospaceparens"></a>
<a id="TOMAUTOSPACEPARENS"></a>


#### tomAutoSpaceParens

<a id="tomDoublestrike"></a>
<a id="tomdoublestrike"></a>
<a id="TOMDOUBLESTRIKE"></a>


#### tomDoublestrike

<a id="tomEmbeddedFont"></a>
<a id="tomembeddedfont"></a>
<a id="TOMEMBEDDEDFONT"></a>


#### tomEmbeddedFont

<a id="tomModWidthPairs"></a>
<a id="tommodwidthpairs"></a>
<a id="TOMMODWIDTHPAIRS"></a>


#### tomModWidthPairs

<a id="tomModWidthSpace"></a>
<a id="tommodwidthspace"></a>
<a id="TOMMODWIDTHSPACE"></a>


#### tomModWidthSpace

<a id="tomOverlapping"></a>
<a id="tomoverlapping"></a>
<a id="TOMOVERLAPPING"></a>


#### tomOverlapping


### -param pMask [out]

Type: <b>long*</b>

The differences in these flags over the range. Zero values indicate that the properties are the same over the range. For an insertion point, this value is always zero.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d2d43bfd-7cdf-458a-822d-e3965bfe2284">ITextFont2</a>



<a href="https://msdn.microsoft.com/a182df7e-2024-48fc-9767-7110ffff0b4c">ITextFont2::GetEffects</a>



<a href="https://msdn.microsoft.com/fb4bfbe3-1e66-41ed-92e6-8d4f3877bdf0">ITextFont2::SetEffects2</a>
 

 

