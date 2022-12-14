---
UID: NF:dwrite.IDWriteTextLayout.SetFontCollection
title: IDWriteTextLayout::SetFontCollection (dwrite.h)
description: Sets the font collection.
helpviewer_keywords: ["IDWriteTextLayout interface [Direct Write]","SetFontCollection method","IDWriteTextLayout.SetFontCollection","IDWriteTextLayout::SetFontCollection","SetFontCollection","SetFontCollection method [Direct Write]","SetFontCollection method [Direct Write]","IDWriteTextLayout interface","directwrite.IDWriteTextLayout_SetFontCollection","dwrite/IDWriteTextLayout::SetFontCollection"]
old-location: directwrite\IDWriteTextLayout_SetFontCollection.htm
tech.root: DirectWrite
ms.assetid: e80038bd-e157-4f76-85c7-559cadacb5c4
ms.date: 12/05/2018
ms.keywords: IDWriteTextLayout interface [Direct Write],SetFontCollection method, IDWriteTextLayout.SetFontCollection, IDWriteTextLayout::SetFontCollection, SetFontCollection, SetFontCollection method [Direct Write], SetFontCollection method [Direct Write],IDWriteTextLayout interface, directwrite.IDWriteTextLayout_SetFontCollection, dwrite/IDWriteTextLayout::SetFontCollection
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
 - IDWriteTextLayout::SetFontCollection
 - dwrite/IDWriteTextLayout::SetFontCollection
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
 - IDWriteTextLayout.SetFontCollection
---

# IDWriteTextLayout::SetFontCollection


## -description

 Sets the font collection.

## -parameters

### -param fontCollection

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection">IDWriteFontCollection</a>*</b>

The font collection to set.

### -param textRange

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a></b>

Text range to which this change applies.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>

