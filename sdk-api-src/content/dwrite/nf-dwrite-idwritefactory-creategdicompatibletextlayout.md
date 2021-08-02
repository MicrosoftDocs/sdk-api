---
UID: NF:dwrite.IDWriteFactory.CreateGdiCompatibleTextLayout
title: IDWriteFactory::CreateGdiCompatibleTextLayout (dwrite.h)
description: Takes a string, format, and associated constraints, and produces an object representing the result, formatted for a particular display resolution and measuring mode.
helpviewer_keywords: ["CreateGdiCompatibleTextLayout","CreateGdiCompatibleTextLayout method [Direct Write]","CreateGdiCompatibleTextLayout method [Direct Write]","IDWriteFactory interface","IDWriteFactory interface [Direct Write]","CreateGdiCompatibleTextLayout method","IDWriteFactory.CreateGdiCompatibleTextLayout","IDWriteFactory::CreateGdiCompatibleTextLayout","directwrite.IDWriteFactory_CreateDisplayTextLayout","dwrite/IDWriteFactory::CreateGdiCompatibleTextLayout"]
old-location: directwrite\IDWriteFactory_CreateDisplayTextLayout.htm
tech.root: DirectWrite
ms.assetid: f9205ce6-1586-461a-9c48-3f3f25780dd0
ms.date: 12/05/2018
ms.keywords: CreateGdiCompatibleTextLayout, CreateGdiCompatibleTextLayout method [Direct Write], CreateGdiCompatibleTextLayout method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateGdiCompatibleTextLayout method, IDWriteFactory.CreateGdiCompatibleTextLayout, IDWriteFactory::CreateGdiCompatibleTextLayout, directwrite.IDWriteFactory_CreateDisplayTextLayout, dwrite/IDWriteFactory::CreateGdiCompatibleTextLayout
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
 - IDWriteFactory::CreateGdiCompatibleTextLayout
 - dwrite/IDWriteFactory::CreateGdiCompatibleTextLayout
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
 - IDWriteFactory.CreateGdiCompatibleTextLayout
---

# IDWriteFactory::CreateGdiCompatibleTextLayout


## -description

 Takes a string, format, and associated constraints,
     and produces an object representing the result, formatted for a particular display resolution
     and measuring mode.

## -parameters

### -param string [in]

Type: <b>const WCHAR*</b>

An array of characters that contains the string to create a new <a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a> object from. This array must be of length <i>stringLength</i> and can contain embedded <b>NULL</b> characters.

### -param stringLength

Type: <b>UINT32</b>

The length of the string, in character count.

### -param textFormat

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a>*</b>

The text formatting object to apply to the string.

### -param layoutWidth

Type: <b>FLOAT</b>

The width of the layout box.

### -param layoutHeight

Type: <b>FLOAT</b>

The height of the layout box.

### -param pixelsPerDip

Type: <b>FLOAT</b>

The number of physical pixels per DIP (device independent pixel). For example, if rendering onto a 96 DPI device <i>pixelsPerDip</i> is 1. If rendering onto a 120 DPI device <i>pixelsPerDip</i> is 1.25 (120/96).

### -param transform [in, optional]

Type: <b>const <a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix">DWRITE_MATRIX</a>*</b>

An optional transform applied to the glyphs and their positions. This transform is applied after the
     scaling specifies the font size and pixels per DIP.

### -param useGdiNatural

Type: <b>BOOL</b>

 Instructs the text layout to use the same metrics as GDI bi-level text when set to <b>FALSE</b>.
     When set to <b>TRUE</b>, instructs the text layout to use the same metrics as text measured by GDI using a font
     created with <b>CLEARTYPE_NATURAL_QUALITY</b>.

### -param textLayout [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>**</b>

When this method returns, contains an address to the pointer of the resultant text layout object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The resulting text layout should only be used for the intended resolution,
     and for cases where text scalability is desired <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createtextlayout">CreateTextLayout</a> should be used instead.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>

