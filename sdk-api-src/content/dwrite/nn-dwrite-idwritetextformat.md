---
UID: NN:dwrite.IDWriteTextFormat
title: IDWriteTextFormat (dwrite.h)
description: The IDWriteTextFormat interface describes the font and paragraph properties used to format text, and it describes locale information.
helpviewer_keywords: ["IDWriteTextFormat","IDWriteTextFormat interface [Direct Write]","IDWriteTextFormat interface [Direct Write]","described","directwrite.IDWriteTextFormat","dwrite/IDWriteTextFormat"]
old-location: directwrite\IDWriteTextFormat.htm
tech.root: DirectWrite
ms.assetid: 64b2cac3-c4cb-4213-b808-7b279d296939
ms.date: 12/05/2018
ms.keywords: IDWriteTextFormat, IDWriteTextFormat interface [Direct Write], IDWriteTextFormat interface [Direct Write],described, directwrite.IDWriteTextFormat, dwrite/IDWriteTextFormat
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
 - IDWriteTextFormat
 - dwrite/IDWriteTextFormat
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
 - IDWriteTextFormat
---

# IDWriteTextFormat interface


## -description

The <b>IDWriteTextFormat</b> interface describes the font and paragraph properties used to format text, and it describes locale information.

## -inheritance

The <b>IDWriteTextFormat</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteTextFormat</b> also has these types of members:

## -remarks

To get a reference to the <b>IDWriteTextFormat</b> interface, the application must call the <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat">IDWriteFactory::CreateTextFormat</a> method as shown in the following code.


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


When creating an <b>IDWriteTextFormat</b> object using the <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextformat">CreateTextFormat</a> function, the application specifies the  font family, font collection, font weight, font size, and locale name for the text format.

These properties cannot be changed after the <b>IDWriteTextFormat</b> object is created.  To change these properties, a new <b>IDWriteTextFormat</b> object must be created with the desired properties.

The <b>IDWriteTextFormat</b> interface is used to draw text with a single format

To draw text with multiple formats, or to use a custom text renderer, use the <a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a> interface.  <b>IDWriteTextLayout</b> enables the application to change the format for ranges of text within the string.  The <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout">IDWriteFactory::CreateTextLayout</a> takes an <b>IDWriteTextFormat</b> object as a parameter and initially applies the format information to the entire string.
      

This object may not be thread-safe, and it may carry the state of text format change.
      

<h3><a id="DirectWrite_and_Direct2D"></a><a id="directwrite_and_direct2d"></a><a id="DIRECTWRITE_AND_DIRECT2D"></a>DirectWrite and Direct2D</h3>
To draw simple text with a single format, <a href="/windows/win32/Direct2D/direct2d-portal">Direct2D</a> provides the  <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)">ID2D1RenderTarget::DrawText</a> method, which draws a string using the format information provided by an <b>IDWriteTextFormat</b> object.

