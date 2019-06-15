---
UID: NF:dwrite_3.IDWriteGdiInterop1.CreateFontFromLOGFONT
title: IDWriteGdiInterop1::CreateFontFromLOGFONT (dwrite_3.h)
author: windows-sdk-content
description: Creates a font object that matches the properties specified by the LOGFONT structure.
old-location: directwrite\idwritegdiinterop1_createfontfromlogfont.htm
tech.root: DirectWrite
ms.assetid: AA28755A-C2E3-4177-A5DD-61D9809A9D0E
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateFontFromLOGFONT, CreateFontFromLOGFONT method [Direct Write], CreateFontFromLOGFONT method [Direct Write],IDWriteGdiInterop1 interface, IDWriteGdiInterop1 interface [Direct Write],CreateFontFromLOGFONT method, IDWriteGdiInterop1.CreateFontFromLOGFONT, IDWriteGdiInterop1::CreateFontFromLOGFONT, directwrite.idwritegdiinterop1_createfontfromlogfont, dwrite_3/IDWriteGdiInterop1::CreateFontFromLOGFONT
ms.topic: method
f1_keywords: ["dwrite_3/IDWriteGdiInterop1.CreateFontFromLOGFONT"]
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IDWriteGdiInterop1.CreateFontFromLOGFONT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteGdiInterop1::CreateFontFromLOGFONT


## -description


Creates a font object that matches the properties specified by the LOGFONT structure.


## -parameters




### -param logFont [in]

Type: <b>LOGFONTW</b>

Structure containing a GDI-compatible font description.


### -param fontCollection [in, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritefontcollection">IDWriteFontCollection</a>*</b>

The font collection to search. If NULL, the local system font collection is used.


### -param font [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritefont">IDWriteFont</a>**</b>

Receives a newly created font object if successful, or NULL in case of error.


## -returns



Type: <b><a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/hh437604(v=vs.85)">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nn-dwrite_3-idwritegdiinterop1">IDWriteGdiInterop1</a>
 

 

