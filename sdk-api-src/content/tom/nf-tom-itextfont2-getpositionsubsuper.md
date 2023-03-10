---
UID: NF:tom.ITextFont2.GetPositionSubSuper
title: ITextFont2::GetPositionSubSuper (tom.h)
description: Gets the subscript or superscript position relative to the baseline.
helpviewer_keywords: ["GetPositionSubSuper","GetPositionSubSuper method [Windows Controls]","GetPositionSubSuper method [Windows Controls]","ITextFont2 interface","ITextFont2 interface [Windows Controls]","GetPositionSubSuper method","ITextFont2.GetPositionSubSuper","ITextFont2::GetPositionSubSuper","controls.itextfont2_getpositionsubsuper","tom/ITextFont2::GetPositionSubSuper"]
old-location: controls\itextfont2_getpositionsubsuper.htm
tech.root: Controls
ms.assetid: c7e53a94-b218-47d1-b366-3bbf7779516e
ms.date: 12/05/2018
ms.keywords: GetPositionSubSuper, GetPositionSubSuper method [Windows Controls], GetPositionSubSuper method [Windows Controls],ITextFont2 interface, ITextFont2 interface [Windows Controls],GetPositionSubSuper method, ITextFont2.GetPositionSubSuper, ITextFont2::GetPositionSubSuper, controls.itextfont2_getpositionsubsuper, tom/ITextFont2::GetPositionSubSuper
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
 - ITextFont2::GetPositionSubSuper
 - tom/ITextFont2::GetPositionSubSuper
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
 - ITextFont2.GetPositionSubSuper
---

# ITextFont2::GetPositionSubSuper


## -description

Gets the subscript or superscript position relative to the baseline.

## -parameters

### -param pValue [out, retval]

Type: <b>long*</b>

The subscript or superscript position relative to the baseline.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the method succeeds, it returns <b>NOERROR</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The subscript or superscript position is relative to the baseline as a percent of the font height.

Subscripts and superscripts in math zones are handled using the <a href="/windows/win32/api/tom/ne-tom-objecttype">tomSubscript</a>, <a href="/windows/win32/api/tom/ne-tom-objecttype">tomSuperscript</a>, <a href="/windows/win32/api/tom/ne-tom-objecttype">tomSubSup</a>, and <a href="/windows/win32/api/tom/ne-tom-objecttype">tomLeftSubSup</a> mathematical objects. See <a href="/windows/desktop/api/tom/nf-tom-itextrange2-getinlineobject">ITextRange2::GetInlineObject</a>.

## -see-also

<a href="/windows/desktop/api/tom/nn-tom-itextfont2">ITextFont2</a>



<a href="/windows/desktop/api/tom/nf-tom-itextfont2-setpositionsubsuper">ITextFont2::SetPositionSubSuper</a>