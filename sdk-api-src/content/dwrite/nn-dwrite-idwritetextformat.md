---
UID: NN:dwrite.IDWriteTextFormat
title: IDWriteTextFormat (dwrite.h)
author: windows-sdk-content
description: The IDWriteTextFormat interface describes the font and paragraph properties used to format text, and it describes locale information.
old-location: directwrite\IDWriteTextFormat.htm
tech.root: DirectWrite
ms.assetid: 64b2cac3-c4cb-4213-b808-7b279d296939
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteTextFormat, IDWriteTextFormat interface [Direct Write], IDWriteTextFormat interface [Direct Write],described, directwrite.IDWriteTextFormat, dwrite/IDWriteTextFormat
ms.topic: interface
f1_keywords: 
 - "dwrite/IDWriteTextFormat"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteTextFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextFormat interface


## -description


The <b>IDWriteTextFormat</b> interface describes the font and paragraph properties used to format text, and it describes locale information.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteTextFormat</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteTextFormat</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteTextFormat</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-getflowdirection">GetFlowDirection</a>
</td>
<td align="left" width="63%">
 Gets the direction that text lines flow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-getfontcollection">GetFontCollection</a>
</td>
<td align="left" width="63%">
 Gets the current font collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-getfontfamilyname">GetFontFamilyName</a>
</td>
<td align="left" width="63%">
 Gets a copy of the font family name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-getfontfamilynamelength">GetFontFamilyNameLength</a>
</td>
<td align="left" width="63%">
 Gets the length of the font family name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-getfontsize">GetFontSize</a>
</td>
<td align="left" width="63%">
 Gets the font  size in DIP unites.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-getfontstretch">GetFontStretch</a>
</td>
<td align="left" width="63%">
 Gets the font stretch of the text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-getfontstyle">GetFontStyle</a>
</td>
<td align="left" width="63%">
 Gets the font style of the text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-getfontweight">GetFontWeight</a>
</td>
<td align="left" width="63%">
 Gets the font weight of the text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-getincrementaltabstop">GetIncrementalTabStop</a>
</td>
<td align="left" width="63%">
 Gets the  incremental tab stop position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-getlinespacing">GetLineSpacing</a>
</td>
<td align="left" width="63%">
 Gets the line spacing adjustment set for a multiline text paragraph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-getlocalename">GetLocaleName</a>
</td>
<td align="left" width="63%">
 Gets a copy of the locale name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-getlocalenamelength">GetLocaleNameLength</a>
</td>
<td align="left" width="63%">
 Gets the length of the locale name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-getparagraphalignment">GetParagraphAlignment</a>
</td>
<td align="left" width="63%">
 Gets the alignment option of a paragraph which is  relative to the top and bottom edges of a layout box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-getreadingdirection">GetReadingDirection</a>
</td>
<td align="left" width="63%">
 Gets the  current reading direction for text in a paragraph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-gettextalignment">GetTextAlignment</a>
</td>
<td align="left" width="63%">
 Gets the alignment option of text relative to the layout box's leading and trailing edge.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-gettrimming">GetTrimming</a>
</td>
<td align="left" width="63%">
 Gets the trimming options for text that overflows the layout box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-getwordwrapping">GetWordWrapping</a>
</td>
<td align="left" width="63%">
 Gets the word wrapping option.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-setflowdirection">SetFlowDirection</a>
</td>
<td align="left" width="63%">
 Sets the  paragraph flow direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-setincrementaltabstop">SetIncrementalTabStop</a>
</td>
<td align="left" width="63%">
 Sets a fixed distance between two adjacent tab stops.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-setlinespacing">SetLineSpacing</a>
</td>
<td align="left" width="63%">
 Sets the  line spacing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment">SetParagraphAlignment</a>
</td>
<td align="left" width="63%">
 Sets the alignment option of a paragraph relative to the layout box's top and bottom edge.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection">SetReadingDirection</a>
</td>
<td align="left" width="63%">
Sets the paragraph reading direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-settextalignment">SetTextAlignment</a>
</td>
<td align="left" width="63%">
Sets the alignment of text in a paragraph, relative to the leading and trailing edge of a layout box for a <b>IDWriteTextFormat</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-settrimming">SetTrimming</a>
</td>
<td align="left" width="63%">
 Sets trimming options for text overflowing the layout width.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-setwordwrapping">SetWordWrapping</a>
</td>
<td align="left" width="63%">
 Sets the word wrapping option.

</td>
</tr>
</table> 


## -remarks



To get a reference to the <b>IDWriteTextFormat</b> interface, the application must call the <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritefactory-createtextformat">IDWriteFactory::CreateTextFormat</a> method as shown in the following code.


```cpp

if (SUCCEEDED(hr))
{
    hr = pDWriteFactory_->CreateTextFormat(
        L"Gabriola",
        NULL,
        DWRITE_FONT_WEIGHT_REGULAR,
        DWRITE_FONT_STYLE_NORMAL,
        DWRITE_FONT_STRETCH_NORMAL,
        72.0f,
        L"en-us",
        &pTextFormat_
        );
}


```


When creating an <b>IDWriteTextFormat</b> object using the <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritefactory-createtextformat">CreateTextFormat</a> function, the application specifies the  font family, font collection, font weight, font size, and locale name for the text format.

These properties cannot be changed after the <b>IDWriteTextFormat</b> object is created.  To change these properties, a new <b>IDWriteTextFormat</b> object must be created with the desired properties.

The <b>IDWriteTextFormat</b> interface is used to draw text with a single format

To draw text with multiple formats, or to use a custom text renderer, use the <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a> interface.  <b>IDWriteTextLayout</b> enables the application to change the format for ranges of text within the string.  The <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritefactory-createtextlayout">IDWriteFactory::CreateTextLayout</a> takes an <b>IDWriteTextFormat</b> object as a parameter and initially applies the format information to the entire string.
      

This object may not be thread-safe, and it may carry the state of text format change.
      

<h3><a id="DirectWrite_and_Direct2D"></a><a id="directwrite_and_direct2d"></a><a id="DIRECTWRITE_AND_DIRECT2D"></a>DirectWrite and Direct2D</h3>
To draw simple text with a single format, <a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> provides the  <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)">ID2D1RenderTarget::DrawText</a> method, which draws a string using the format information provided by an <b>IDWriteTextFormat</b> object.



