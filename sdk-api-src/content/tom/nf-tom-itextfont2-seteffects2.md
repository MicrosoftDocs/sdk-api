---
UID: NF:tom.ITextFont2.SetEffects2
title: ITextFont2::SetEffects2 (tom.h)
description: Sets the additional character format effects.
helpviewer_keywords: ["ITextFont2 interface [Windows Controls]","SetEffects2 method","ITextFont2.SetEffects2","ITextFont2::SetEffects2","SetEffects2","SetEffects2 method [Windows Controls]","SetEffects2 method [Windows Controls]","ITextFont2 interface","controls.itextfont2_seteffects2","tom/ITextFont2::SetEffects2","tomAutoSpaceAlpha","tomAutoSpaceNumeric","tomAutoSpaceParens","tomDoublestrike","tomEmbeddedFont","tomModWidthPairs","tomModWidthSpace","tomOverlapping"]
old-location: controls\itextfont2_seteffects2.htm
tech.root: Controls
ms.assetid: fb4bfbe3-1e66-41ed-92e6-8d4f3877bdf0
ms.date: 12/05/2018
ms.keywords: ITextFont2 interface [Windows Controls],SetEffects2 method, ITextFont2.SetEffects2, ITextFont2::SetEffects2, SetEffects2, SetEffects2 method [Windows Controls], SetEffects2 method [Windows Controls],ITextFont2 interface, controls.itextfont2_seteffects2, tom/ITextFont2::SetEffects2, tomAutoSpaceAlpha, tomAutoSpaceNumeric, tomAutoSpaceParens, tomDoublestrike, tomEmbeddedFont, tomModWidthPairs, tomModWidthSpace, tomOverlapping
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
 - ITextFont2::SetEffects2
 - tom/ITextFont2::SetEffects2
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
 - ITextFont2.SetEffects2
---

# ITextFont2::SetEffects2


## -description

Sets the additional character format effects.

## -parameters

### -param Value [in]

Type: <b>long</b>

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

### -param Mask [in]

Type: <b>long</b>

The desired mask, which can be a combination of the <i>Value</i> flags. Only effects with the corresponding mask flag set are modified.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Only effects with the corresponding mask flag set are modified.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-geteffects2">ITextFont2::GetEffects2</a>