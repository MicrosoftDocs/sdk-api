---
UID: NF:dwrite_3.IDWriteFontList1.GetFont
title: IDWriteFontList1::GetFont (dwrite_3.h)
description: Gets a font given its zero-based index.
helpviewer_keywords: ["GetFont","GetFont method [Direct Write]","GetFont method [Direct Write]","IDWriteFontList1 interface","IDWriteFontList1 interface [Direct Write]","GetFont method","IDWriteFontList1.GetFont","IDWriteFontList1::GetFont","directwrite.idwritefontlist1_getfont","dwrite_3/IDWriteFontList1::GetFont"]
old-location: directwrite\idwritefontlist1_getfont.htm
tech.root: DirectWrite
ms.assetid: 206A103C-5847-4388-83EC-BE038DB20A09
ms.date: 12/05/2018
ms.keywords: GetFont, GetFont method [Direct Write], GetFont method [Direct Write],IDWriteFontList1 interface, IDWriteFontList1 interface [Direct Write],GetFont method, IDWriteFontList1.GetFont, IDWriteFontList1::GetFont, directwrite.idwritefontlist1_getfont, dwrite_3/IDWriteFontList1::GetFont
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IDWriteFontList1::GetFont
 - dwrite_3/IDWriteFontList1::GetFont
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
 - IDWriteFontList1.GetFont
---

# IDWriteFontList1::GetFont


## -description

Gets a font given its zero-based index.

## -parameters

### -param listIndex [in]

Type: <b>UINT32</b>

Zero-based index of the font in the font list.

### -param font [out]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefont3">IDWriteFont3</a>**</b>

A pointer to a memory block that receives a pointer to a <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefont3">IDWriteFont3</a> interface for the newly created font object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.



This method returns <b>DWRITE_E_REMOTEFONT</b> if it could not construct a remote font.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist1">IDWriteFontList1</a>

