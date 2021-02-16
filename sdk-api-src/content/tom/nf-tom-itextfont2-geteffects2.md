---
UID: NF:tom.ITextFont2.GetEffects2
title: ITextFont2::GetEffects2 (tom.h)
description: Gets the additional character format effects.
helpviewer_keywords: ["GetEffects2","GetEffects2 method [Windows Controls]","GetEffects2 method [Windows Controls]","ITextFont2 interface","ITextFont2 interface [Windows Controls]","GetEffects2 method","ITextFont2.GetEffects2","ITextFont2::GetEffects2","controls.itextfont2_geteffects2","tom/ITextFont2::GetEffects2","tomAutoSpaceAlpha","tomAutoSpaceNumeric","tomAutoSpaceParens","tomDoublestrike","tomEmbeddedFont","tomModWidthPairs","tomModWidthSpace","tomOverlapping"]
old-location: controls\itextfont2_geteffects2.htm
tech.root: Controls
ms.assetid: 6b28c995-33dd-4f5b-ac89-eec367e0a4d5
ms.date: 12/05/2018
ms.keywords: GetEffects2, GetEffects2 method [Windows Controls], GetEffects2 method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetEffects2 method, ITextFont2.GetEffects2, ITextFont2::GetEffects2, controls.itextfont2_geteffects2, tom/ITextFont2::GetEffects2, tomAutoSpaceAlpha, tomAutoSpaceNumeric, tomAutoSpaceParens, tomDoublestrike, tomEmbeddedFont, tomModWidthPairs, tomModWidthSpace, tomOverlapping
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
req.lib: 
req.dll: Msftedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextFont2::GetEffects2
 - tom/ITextFont2::GetEffects2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextFont2.GetEffects2
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

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-geteffects">ITextFont2::GetEffects</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-seteffects2">ITextFont2::SetEffects2</a>