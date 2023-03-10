---
UID: NF:dwrite.IDWriteTextLayout.SetFontStyle
title: IDWriteTextLayout::SetFontStyle (dwrite.h)
description: Sets the font style for text within a text range specified by a DWRITE_TEXT_RANGE structure.
helpviewer_keywords: ["IDWriteTextLayout interface [Direct Write]","SetFontStyle method","IDWriteTextLayout.SetFontStyle","IDWriteTextLayout::SetFontStyle","SetFontStyle","SetFontStyle method [Direct Write]","SetFontStyle method [Direct Write]","IDWriteTextLayout interface","directwrite.IDWriteTextLayout_SetFontStyle","dwrite/IDWriteTextLayout::SetFontStyle"]
old-location: directwrite\IDWriteTextLayout_SetFontStyle.htm
tech.root: DirectWrite
ms.assetid: 688a6c30-5eca-44aa-bcb0-02a3f29647b8
ms.date: 12/05/2018
ms.keywords: IDWriteTextLayout interface [Direct Write],SetFontStyle method, IDWriteTextLayout.SetFontStyle, IDWriteTextLayout::SetFontStyle, SetFontStyle, SetFontStyle method [Direct Write], SetFontStyle method [Direct Write],IDWriteTextLayout interface, directwrite.IDWriteTextLayout_SetFontStyle, dwrite/IDWriteTextLayout::SetFontStyle
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
 - IDWriteTextLayout::SetFontStyle
 - dwrite/IDWriteTextLayout::SetFontStyle
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
 - IDWriteTextLayout.SetFontStyle
---

# IDWriteTextLayout::SetFontStyle


## -description

 Sets the font style for  text within a text range specified by a <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a> structure.

## -parameters

### -param fontStyle

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style">DWRITE_FONT_STYLE</a></b>

The  font style to be set   for text within a range specified by <i>textRange</i>.

### -param textRange

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a></b>

The text range to which this change applies.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The font style can be set to Normal, Italic or Oblique. The following illustration shows  three styles for the Palatino font.  For more information, see <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style">DWRITE_FONT_STYLE</a>.

<img alt="Illustration of normal, italic, and oblique font styles for the Palatino font" src="./images/FontStyle_for_Palatino.png"/>


#### Examples

The following code illustrates how to set the font style to italic.


```cpp

// Set the font style to italic for the entire string.
DWRITE_TEXT_RANGE textRange = {0, cTextLength_};

if (SUCCEEDED(hr))
{
    hr = pTextLayout_->SetFontStyle(DWRITE_FONT_STYLE_ITALIC, textRange);
}


```

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>

