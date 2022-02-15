---
UID: NF:dwrite.IDWriteFontList.GetFontCollection
title: IDWriteFontList::GetFontCollection (dwrite.h)
description: Gets the font collection that contains the fonts in the font list.
helpviewer_keywords: ["GetFontCollection","GetFontCollection method [Direct Write]","GetFontCollection method [Direct Write]","IDWriteFontList interface","IDWriteFontList interface [Direct Write]","GetFontCollection method","IDWriteFontList.GetFontCollection","IDWriteFontList::GetFontCollection","directwrite.IDWriteFontList_GetFontCollection","dwrite/IDWriteFontList::GetFontCollection"]
old-location: directwrite\IDWriteFontList_GetFontCollection.htm
tech.root: DirectWrite
ms.assetid: f3c13a33-7bf7-4027-af10-f4863008cef2
ms.date: 12/05/2018
ms.keywords: GetFontCollection, GetFontCollection method [Direct Write], GetFontCollection method [Direct Write],IDWriteFontList interface, IDWriteFontList interface [Direct Write],GetFontCollection method, IDWriteFontList.GetFontCollection, IDWriteFontList::GetFontCollection, directwrite.IDWriteFontList_GetFontCollection, dwrite/IDWriteFontList::GetFontCollection
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
 - IDWriteFontList::GetFontCollection
 - dwrite/IDWriteFontList::GetFontCollection
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
 - IDWriteFontList.GetFontCollection
---

# IDWriteFontList::GetFontCollection


## -description

 Gets the font collection that contains the fonts in
    the font list.

## -parameters

### -param fontCollection [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection">IDWriteFontCollection</a>**</b>

When this method returns, contains the address of a pointer to the current <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection">IDWriteFontCollection</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontlist">IDWriteFontList</a>

