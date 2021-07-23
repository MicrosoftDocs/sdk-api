---
UID: NF:dwrite.IDWriteTextLayout.SetFontWeight
title: IDWriteTextLayout::SetFontWeight (dwrite.h)
description: Sets the font weight for text within a text range specified by a DWRITE_TEXT_RANGE structure.
helpviewer_keywords: ["IDWriteTextLayout interface [Direct Write]","SetFontWeight method","IDWriteTextLayout.SetFontWeight","IDWriteTextLayout::SetFontWeight","SetFontWeight","SetFontWeight method [Direct Write]","SetFontWeight method [Direct Write]","IDWriteTextLayout interface","directwrite.IDWriteTextLayout_SetFontWeight","dwrite/IDWriteTextLayout::SetFontWeight"]
old-location: directwrite\IDWriteTextLayout_SetFontWeight.htm
tech.root: DirectWrite
ms.assetid: c6b65548-c486-4006-afe9-95bc628bbf70
ms.date: 12/05/2018
ms.keywords: IDWriteTextLayout interface [Direct Write],SetFontWeight method, IDWriteTextLayout.SetFontWeight, IDWriteTextLayout::SetFontWeight, SetFontWeight, SetFontWeight method [Direct Write], SetFontWeight method [Direct Write],IDWriteTextLayout interface, directwrite.IDWriteTextLayout_SetFontWeight, dwrite/IDWriteTextLayout::SetFontWeight
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteTextLayout::SetFontWeight
 - dwrite/IDWriteTextLayout::SetFontWeight
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteTextLayout.SetFontWeight
---

# IDWriteTextLayout::SetFontWeight


## -description

 Sets the font weight for text within a text range specified by a <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a> structure.

## -parameters

### -param fontWeight

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight">DWRITE_FONT_WEIGHT</a></b>

The font weight to be set for text within the range specified by <i>textRange</i>.

### -param textRange

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a></b>

Text range to which this change applies.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The font weight can be set to one of the predefined font weight values provided in the <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight">DWRITE_FONT_WEIGHT</a> enumeration or an integer from 1 to 999.  Values outside this range will cause the method to fail with an <b>E_INVALIDARG</b> return value.

The following illustration shows an example of Normal and UltraBold weights for the Palatino Linotype typeface.

<img alt='Illustration of the letter "W" in Normal and UltraBold weights' src="./images/FontWeight_for_Palatino.png"/>

#### Examples

The following code illustrates how to set the font weight to bold.


```cpp

// Set the font weight to bold for the entire string.
DWRITE_TEXT_RANGE textRange = {0, cTextLength_};

if (SUCCEEDED(hr))
{
    hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
}


```

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>

