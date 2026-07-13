---
UID: NF:dwrite_3.IDWriteFontCollection2.GetFontSet
title: IDWriteFontCollection2::GetFontSet
description: Retrieves the underlying font set used by this collection.
helpviewer_keywords: ["IDWriteFontCollection2 interface [Direct Write]","GetFontSet method","IDWriteFontCollection2.GetFontSet","IDWriteFontCollection2::GetFontSet","GetFontSet","GetFontSet method [Direct Write]","GetFontSet method [Direct Write]","IDWriteFontCollection2 interface","directwrite.idwritefontcollection2_getfontset","dwrite_3/IDWriteFontCollection2::GetFontSet"]
tech.root: DirectWrite
ms.date: 09/10/2025
ms.keywords: IDWriteFontCollection2 interface [Direct Write],GetFontSet method, IDWriteFontCollection2.GetFontSet, IDWriteFontCollection2::GetFontSet, GetFontSet, GetFontSet method [Direct Write], GetFontSet method [Direct Write],IDWriteFontCollection2 interface, directwrite.idwritefontcollection2_getfontset, dwrite_3/IDWriteFontCollection2::GetFontSet
req.construct-type: function
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 16299
req.target-min-winversvr: Windows 10 Build 16299
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - IDWriteFontCollection2::GetFontSet
 - dwrite_3/IDWriteFontCollection2::GetFontSet
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteFontCollection2::GetFontSet
---

## -description

Retrieves the underlying font set used by this collection.

## -parameters

### -param fontSet [out]

Type: **[IDWriteFontSet1](./nn-dwrite_3-idwritefontset1.md)\*\***

The address of a pointer to an [IDWriteFontSet1](./nn-dwrite_3-idwritefontset1.md) interface. On successful completion, the function sets the pointer to the font set used by the collection.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

## -see-also
