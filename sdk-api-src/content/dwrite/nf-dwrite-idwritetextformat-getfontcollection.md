---
UID: NF:dwrite.IDWriteTextFormat.GetFontCollection
title: IDWriteTextFormat::GetFontCollection (dwrite.h)
description: Gets the current font collection.
helpviewer_keywords: ["GetFontCollection","GetFontCollection method [Direct Write]","GetFontCollection method [Direct Write]","IDWriteTextFormat interface","IDWriteTextFormat interface [Direct Write]","GetFontCollection method","IDWriteTextFormat.GetFontCollection","IDWriteTextFormat::GetFontCollection","directwrite.IDWriteTextFormat_GetFontCollection","dwrite/IDWriteTextFormat::GetFontCollection"]
old-location: directwrite\IDWriteTextFormat_GetFontCollection.htm
tech.root: DirectWrite
ms.assetid: a94cfca5-3a03-4912-9a33-df705a2265cf
ms.date: 12/05/2018
ms.keywords: GetFontCollection, GetFontCollection method [Direct Write], GetFontCollection method [Direct Write],IDWriteTextFormat interface, IDWriteTextFormat interface [Direct Write],GetFontCollection method, IDWriteTextFormat.GetFontCollection, IDWriteTextFormat::GetFontCollection, directwrite.IDWriteTextFormat_GetFontCollection, dwrite/IDWriteTextFormat::GetFontCollection
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
 - IDWriteTextFormat::GetFontCollection
 - dwrite/IDWriteTextFormat::GetFontCollection
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
 - IDWriteTextFormat.GetFontCollection
---

# IDWriteTextFormat::GetFontCollection


## -description

 Gets the current font collection.

## -parameters

### -param fontCollection [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection">IDWriteFontCollection</a>**</b>

When this method returns, contains an address of a pointer to the font collection being used for the current text.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a>

