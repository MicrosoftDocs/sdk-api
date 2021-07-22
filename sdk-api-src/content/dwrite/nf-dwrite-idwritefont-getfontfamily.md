---
UID: NF:dwrite.IDWriteFont.GetFontFamily
title: IDWriteFont::GetFontFamily (dwrite.h)
description: Gets the font family to which the specified font belongs.
helpviewer_keywords: ["GetFontFamily","GetFontFamily method [Direct Write]","GetFontFamily method [Direct Write]","IDWriteFont interface","IDWriteFont interface [Direct Write]","GetFontFamily method","IDWriteFont.GetFontFamily","IDWriteFont::GetFontFamily","directwrite.IDWriteFont_GetFontFamily","dwrite/IDWriteFont::GetFontFamily"]
old-location: directwrite\IDWriteFont_GetFontFamily.htm
tech.root: DirectWrite
ms.assetid: 6104a8ed-378f-4e2b-a0e5-8c0291750e65
ms.date: 12/05/2018
ms.keywords: GetFontFamily, GetFontFamily method [Direct Write], GetFontFamily method [Direct Write],IDWriteFont interface, IDWriteFont interface [Direct Write],GetFontFamily method, IDWriteFont.GetFontFamily, IDWriteFont::GetFontFamily, directwrite.IDWriteFont_GetFontFamily, dwrite/IDWriteFont::GetFontFamily
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
 - IDWriteFont::GetFontFamily
 - dwrite/IDWriteFont::GetFontFamily
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
 - IDWriteFont.GetFontFamily
---

# IDWriteFont::GetFontFamily


## -description

 Gets the font family to which the specified font belongs.

## -parameters

### -param fontFamily [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily">IDWriteFontFamily</a>**</b>

When this method returns, contains an address of a pointer to the font family object to which the specified font belongs.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefont">IDWriteFont</a>

