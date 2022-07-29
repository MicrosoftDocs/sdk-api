---
UID: NF:dwrite.IDWriteFactory.CreateTextFormat
title: IDWriteFactory::CreateTextFormat (dwrite.h)
description: Creates a text format object used for text layout. (IDWriteFactory.CreateTextFormat)
helpviewer_keywords: ["CreateTextFormat","CreateTextFormat method [Direct Write]","CreateTextFormat method [Direct Write]","IDWriteFactory interface","IDWriteFactory interface [Direct Write]","CreateTextFormat method","IDWriteFactory.CreateTextFormat","IDWriteFactory::CreateTextFormat","directwrite.IDWriteFactory_CreateTextFormat","dwrite/IDWriteFactory::CreateTextFormat"]
old-location: directwrite\IDWriteFactory_CreateTextFormat.htm
tech.root: DirectWrite
ms.assetid: d6e7caba-5cba-4b6e-b146-10aa6d21cac1
ms.date: 12/05/2018
ms.keywords: CreateTextFormat, CreateTextFormat method [Direct Write], CreateTextFormat method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateTextFormat method, IDWriteFactory.CreateTextFormat, IDWriteFactory::CreateTextFormat, directwrite.IDWriteFactory_CreateTextFormat, dwrite/IDWriteFactory::CreateTextFormat
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
 - IDWriteFactory::CreateTextFormat
 - dwrite/IDWriteFactory::CreateTextFormat
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
 - IDWriteFactory.CreateTextFormat
---

# IDWriteFactory::CreateTextFormat


## -description

 Creates a text format object used for text layout.

## -parameters

### -param fontFamilyName [in]

Type: <b>const WCHAR*</b>

An array of characters that contains the name of the font family

### -param fontCollection

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection">IDWriteFontCollection</a>*</b>

A pointer to a font collection object. When this is <b>NULL</b>, indicates the system font collection.

### -param fontWeight

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight">DWRITE_FONT_WEIGHT</a></b>

A value that indicates the font weight for the text object created by this method.

### -param fontStyle

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style">DWRITE_FONT_STYLE</a></b>

A value that indicates the font style for the text object created by this method.

### -param fontStretch

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch">DWRITE_FONT_STRETCH</a></b>

A value that indicates the font stretch for the text object created by this method.

### -param fontSize

Type: <b>FLOAT</b>

The logical size of the font in DIP ("device-independent pixel") units. A DIP equals 1/96 inch.

### -param localeName [in]

Type: <b>const WCHAR*</b>

An array of characters that contains the locale name.

### -param textFormat [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a>**</b>

When this method returns, contains an address of a pointer to a  newly created text format object, or <b>NULL</b> in case of failure.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>

