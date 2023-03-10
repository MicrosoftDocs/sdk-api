---
UID: NF:dwrite.IDWriteTextLayout.GetFontCollection
title: IDWriteTextLayout::GetFontCollection (dwrite.h)
description: Gets the font collection associated with the text at the specified position.
helpviewer_keywords: ["GetFontCollection","GetFontCollection method [Direct Write]","GetFontCollection method [Direct Write]","IDWriteTextLayout interface","IDWriteTextLayout interface [Direct Write]","GetFontCollection method","IDWriteTextLayout.GetFontCollection","IDWriteTextLayout::GetFontCollection","directwrite.IDWriteTextLayout_GetFontCollection","dwrite/IDWriteTextLayout::GetFontCollection"]
old-location: directwrite\IDWriteTextLayout_GetFontCollection.htm
tech.root: DirectWrite
ms.assetid: ce3e4510-2b40-4eb4-aaf8-fe830e96d618
ms.date: 12/05/2018
ms.keywords: GetFontCollection, GetFontCollection method [Direct Write], GetFontCollection method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetFontCollection method, IDWriteTextLayout.GetFontCollection, IDWriteTextLayout::GetFontCollection, directwrite.IDWriteTextLayout_GetFontCollection, dwrite/IDWriteTextLayout::GetFontCollection
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
 - IDWriteTextLayout::GetFontCollection
 - dwrite/IDWriteTextLayout::GetFontCollection
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
 - IDWriteTextLayout.GetFontCollection
---

# IDWriteTextLayout::GetFontCollection


## -description

 Gets the font collection associated with the text at the specified position.

## -parameters

### -param currentPosition

Type: <b>UINT32</b>

The position of the text to inspect.

### -param fontCollection [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection">IDWriteFontCollection</a>**</b>

Contains an address of a  pointer to the current font collection.

### -param textRange [out, optional]

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a>*</b>

The range of text that has the same  formatting as the text at the position specified by <i>currentPosition</i>.  This means the run has the exact  formatting as the position specified, including but not limited to the underline.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>

