---
UID: NN:dwrite.IDWriteTextFormat
title: IDWriteTextFormat
author: windows-sdk-content
description: The IDWriteTextFormat interface describes the font and paragraph properties used to format text, and it describes locale information.
old-location: directwrite\IDWriteTextFormat.htm
tech.root: DirectWrite
ms.assetid: 64b2cac3-c4cb-4213-b808-7b279d296939
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDWriteTextFormat, IDWriteTextFormat interface [Direct Write], IDWriteTextFormat interface [Direct Write],described, directwrite.IDWriteTextFormat, dwrite/IDWriteTextFormat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
---

# IDWriteTextFormat interface


## -description


The <b>IDWriteTextFormat</b> interface describes the font and paragraph properties used to format text, and it describes locale information.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteTextFormat</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteTextFormat</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/993eb17b-a03a-44f7-b273-a0746db3ed70">GetFlowDirection</a>
</td>
<td align="left" width="63%">
 Gets the direction that text lines flow.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a94cfca5-3a03-4912-9a33-df705a2265cf">GetFontCollection</a>
</td>
<td align="left" width="63%">
 Gets the current font collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44d294bf-ec0f-4c75-b10a-2f3e4883b58a">GetFontFamilyName</a>
</td>
<td align="left" width="63%">
 Gets a copy of the font family name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bf57fc7-ba5e-44dd-8dd1-47e759842a57">GetFontFamilyNameLength</a>
</td>
<td align="left" width="63%">
 Gets the length of the font family name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4676d35c-62c2-478c-9ccd-68ed53cba71c">GetFontSize</a>
</td>
<td align="left" width="63%">
 Gets the font  size in DIP unites.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57ff471d-5daa-4657-8bfa-1fd6e173411f">GetFontStretch</a>
</td>
<td align="left" width="63%">
 Gets the font stretch of the text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53a52196-6640-46b1-afdf-ee5ba9e1ef11">GetFontStyle</a>
</td>
<td align="left" width="63%">
 Gets the font style of the text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e8a504e-3afa-4b12-92f8-e2fd7d535bb5">GetFontWeight</a>
</td>
<td align="left" width="63%">
 Gets the font weight of the text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/080c9fe3-3323-4e30-8dbc-fe44e874cf6d">GetIncrementalTabStop</a>
</td>
<td align="left" width="63%">
 Gets the  incremental tab stop position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9563d4d-0b7d-4921-b251-6ef1e24105f1">GetLineSpacing</a>
</td>
<td align="left" width="63%">
 Gets the line spacing adjustment set for a multiline text paragraph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/89b35622-0898-4fc5-9871-b75244e4dba6">GetLocaleName</a>
</td>
<td align="left" width="63%">
 Gets a copy of the locale name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/197926ad-ff96-48b3-872b-22a683725ef8">GetLocaleNameLength</a>
</td>
<td align="left" width="63%">
 Gets the length of the locale name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c05e1b59-0263-45a7-872c-b44b04858a5a">GetParagraphAlignment</a>
</td>
<td align="left" width="63%">
 Gets the alignment option of a paragraph which is  relative to the top and bottom edges of a layout box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b89cfbab-5063-4c1b-92a8-d8ba067f7148">GetReadingDirection</a>
</td>
<td align="left" width="63%">
 Gets the  current reading direction for text in a paragraph.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b6d58d8-2ddb-4e60-95ac-27a1aeec7602">GetTextAlignment</a>
</td>
<td align="left" width="63%">
 Gets the alignment option of text relative to the layout box's leading and trailing edge.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6147d0a4-8f50-40c6-864e-734cfef57089">GetTrimming</a>
</td>
<td align="left" width="63%">
 Gets the trimming options for text that overflows the layout box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3ce0513-da7e-4645-b677-52dcd2a060d4">GetWordWrapping</a>
</td>
<td align="left" width="63%">
 Gets the word wrapping option.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0eb1648c-b565-46e8-b6db-1fcc6a66b1bd">SetFlowDirection</a>
</td>
<td align="left" width="63%">
 Sets the  paragraph flow direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dec68000-2172-4367-a22e-fbc3b3e84851">SetIncrementalTabStop</a>
</td>
<td align="left" width="63%">
 Sets a fixed distance between two adjacent tab stops.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3629779a-5e50-43ea-b161-dd17598b5b43">SetLineSpacing</a>
</td>
<td align="left" width="63%">
 Sets the  line spacing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6eb8aea-3945-471d-a34a-c2f3221dfeaf">SetParagraphAlignment</a>
</td>
<td align="left" width="63%">
 Sets the alignment option of a paragraph relative to the layout box's top and bottom edge.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb26241c-e97e-43d3-9f0a-0a9f932d8483">SetReadingDirection</a>
</td>
<td align="left" width="63%">
Sets the paragraph reading direction.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e7554e3-4e0c-45b1-a874-a3054b0e91dc">SetTextAlignment</a>
</td>
<td align="left" width="63%">
Sets the alignment of text in a paragraph, relative to the leading and trailing edge of a layout box for a <b>IDWriteTextFormat</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/737eab93-2761-4a59-81e8-ef827be30325">SetTrimming</a>
</td>
<td align="left" width="63%">
 Sets trimming options for text overflowing the layout width.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04c9fc62-d5a3-470b-bcae-4c6570eebdaa">SetWordWrapping</a>
</td>
<td align="left" width="63%">
 Sets the word wrapping option.

</td>
</tr>
</table> 


## -remarks



To get a reference to the <b>IDWriteTextFormat</b> interface, the application must call the <a href="https://msdn.microsoft.com/d6e7caba-5cba-4b6e-b146-10aa6d21cac1">IDWriteFactory::CreateTextFormat</a> method as shown in the following code.


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


When creating an <b>IDWriteTextFormat</b> object using the <a href="https://msdn.microsoft.com/d6e7caba-5cba-4b6e-b146-10aa6d21cac1">CreateTextFormat</a> function, the application specifies the  font family, font collection, font weight, font size, and locale name for the text format.

These properties cannot be changed after the <b>IDWriteTextFormat</b> object is created.  To change these properties, a new <b>IDWriteTextFormat</b> object must be created with the desired properties.

The <b>IDWriteTextFormat</b> interface is used to draw text with a single format

To draw text with multiple formats, or to use a custom text renderer, use the <a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a> interface.  <b>IDWriteTextLayout</b> enables the application to change the format for ranges of text within the string.  The <a href="https://msdn.microsoft.com/f76f85df-112f-4bc3-b922-a0d7940d2954">IDWriteFactory::CreateTextLayout</a> takes an <b>IDWriteTextFormat</b> object as a parameter and initially applies the format information to the entire string.
      

This object may not be thread-safe, and it may carry the state of text format change.
      

<h3><a id="DirectWrite_and_Direct2D"></a><a id="directwrite_and_direct2d"></a><a id="DIRECTWRITE_AND_DIRECT2D"></a>DirectWrite and Direct2D</h3>
To draw simple text with a single format, <a href="https://msdn.microsoft.com/03b3b91c-9751-4f8d-af24-85067f06930b">Direct2D</a> provides the  <a href="https://msdn.microsoft.com/226de985-0d7a-4891-83a0-b1f022ff8bd3">ID2D1RenderTarget::DrawText</a> method, which draws a string using the format information provided by an <b>IDWriteTextFormat</b> object.



