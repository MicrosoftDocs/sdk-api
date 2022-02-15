---
UID: NN:dwrite.IDWriteTextLayout
title: IDWriteTextLayout (dwrite.h)
description: The IDWriteTextLayout interface represents a block of text after it has been fully analyzed and formatted.
helpviewer_keywords: ["IDWriteTextLayout","IDWriteTextLayout interface [Direct Write]","IDWriteTextLayout interface [Direct Write]","described","directwrite.IDWriteTextLayout","dwrite/IDWriteTextLayout"]
old-location: directwrite\IDWriteTextLayout.htm
tech.root: DirectWrite
ms.assetid: 0d687337-8623-4014-967c-f533072e31cc
ms.date: 12/05/2018
ms.keywords: IDWriteTextLayout, IDWriteTextLayout interface [Direct Write], IDWriteTextLayout interface [Direct Write],described, directwrite.IDWriteTextLayout, dwrite/IDWriteTextLayout
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
 - IDWriteTextLayout
 - dwrite/IDWriteTextLayout
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
 - IDWriteTextLayout
---

# IDWriteTextLayout interface


## -description

The <b>IDWriteTextLayout</b> interface represents a block of text after it has been fully analyzed and formatted.

## -inheritance

The <b>IDWriteTextLayout</b> interface inherits from <a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a>. <b>IDWriteTextLayout</b> also has these types of members:

## -remarks

To get a reference to the <b>IDWriteTextLayout</b> interface, the application must call the <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout">IDWriteFactory::CreateTextLayout</a> method, as shown in the following code.  


```cpp

// Create a text layout using the text format.
if (SUCCEEDED(hr))
{
    RECT rect;
    GetClientRect(hwnd_, &rect); 
    float width  = rect.right  / dpiScaleX_;
    float height = rect.bottom / dpiScaleY_;

    hr = pDWriteFactory_->CreateTextLayout(
        wszText_,      // The string to be laid out and formatted.
        cTextLength_,  // The length of the string.
        pTextFormat_,  // The text format to apply to the string (contains font information, etc).
        width,         // The width of the layout box.
        height,        // The height of the layout box.
        &pTextLayout_  // The IDWriteTextLayout interface pointer.
        );
}


```


The <b>IDWriteTextLayout</b> interface allows the application to change the format for ranges of the text it represents, specified by a <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a> structure.   The following example shows how to set the font weight for a text range.


```cpp

// Set the font weight to bold for the first 5 letters.
DWRITE_TEXT_RANGE textRange = {0, 4};

if (SUCCEEDED(hr))
{
    hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
}


```


<b>IDWriteTextLayout</b> also provides methods for adding strikethrough,  underline, and inline objects to the text.

To draw the block of text represented by an <b>IDWriteTextLayout</b> object, <a href="/windows/win32/Direct2D/direct2d-portal">Direct2D</a> provides the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout">ID2D1RenderTarget::DrawTextLayout</a> method. To draw using a custom renderer implement an <a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer">IDWriteTextRenderer</a> interface and  call the  <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw">IDWriteTextLayout::Draw</a> method

<h3><a id="DirectWrite_and_Direct2D"></a><a id="directwrite_and_direct2d"></a><a id="DIRECTWRITE_AND_DIRECT2D"></a>DirectWrite and Direct2D</h3>
To draw a formatted string represented by an <b>IDWriteTextLayout</b> object, <a href="/windows/win32/Direct2D/direct2d-portal">Direct2D</a> provides the  <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout">ID2D1RenderTarget::DrawTextLayout</a> method.

<h3><a id="Other_Rendering_Options"></a><a id="other_rendering_options"></a><a id="OTHER_RENDERING_OPTIONS"></a>Other Rendering Options</h3>
To render using a custom renderer, use the <a href="/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw">IDWriteTextLayout::Draw</a> method, which takes a callback interface derived from <a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer">IDWriteTextRenderer</a> as an argument, as shown in the following code.


```cpp

// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );


```



<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer">IDWriteTextRenderer</a> declares methods for drawing a glyph run, underline, strikethrough and inline objects.  It is up to the application to implement these methods.  Creating a custom text renderer allows the application to apply additional effects when rendering text, such as a custom fill or outline.

Using a custom text renderer also enables you to render using another technology, such as GDI.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a>

