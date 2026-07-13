---
UID: NF:dwrite.IDWriteFontList.GetFont
title: IDWriteFontList::GetFont (dwrite.h)
description: Gets a font given its zero-based index. (IDWriteFontList.GetFont)
helpviewer_keywords: ["GetFont","GetFont method [Direct Write]","GetFont method [Direct Write]","IDWriteFontList interface","IDWriteFontList interface [Direct Write]","GetFont method","IDWriteFontList.GetFont","IDWriteFontList::GetFont","directwrite.IDWriteFontList_GetFont","dwrite/IDWriteFontList::GetFont"]
old-location: directwrite\IDWriteFontList_GetFont.htm
tech.root: DirectWrite
ms.assetid: b2262707-b5d5-4697-9634-72fd2a72000a
ms.date: 12/05/2018
ms.keywords: GetFont, GetFont method [Direct Write], GetFont method [Direct Write],IDWriteFontList interface, IDWriteFontList interface [Direct Write],GetFont method, IDWriteFontList.GetFont, IDWriteFontList::GetFont, directwrite.IDWriteFontList_GetFont, dwrite/IDWriteFontList::GetFont
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
 - IDWriteFontList::GetFont
 - dwrite/IDWriteFontList::GetFont
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
 - IDWriteFontList.GetFont
---

# IDWriteFontList::GetFont


## -description

 Gets a font given its zero-based index.

## -parameters

### -param index

Type: <b>UINT32</b>

Zero-based index of the font in the font list.

### -param font [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefont">IDWriteFont</a>**</b>

When this method returns, contains the address of a pointer to the newly created <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefont">IDWriteFont</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontlist">IDWriteFontList</a>

