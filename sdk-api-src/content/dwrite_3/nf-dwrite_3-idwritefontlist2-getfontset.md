---
UID: NF:dwrite_3.IDWriteFontList2.GetFontSet
title: IDWriteFontList2::GetFontSet
description: Retrieves the underlying font set used by this list.
helpviewer_keywords: ["IDWriteFontList2 interface [Direct Write]","GetFontSet method","IDWriteFontList2.GetFontSet","IDWriteFontList2::GetFontSet","GetFontSet","GetFontSet method [Direct Write]","GetFontSet method [Direct Write]","IDWriteFontList2 interface","directwrite.idwritefontlist2_getfontset","dwrite_3/IDWriteFontList2::GetFontSet"]
tech.root: DirectWrite
ms.date: 09/13/2019
ms.keywords: IDWriteFontList2 interface [Direct Write],GetFontSet method, IDWriteFontList2.GetFontSet, IDWriteFontList2::GetFontSet, GetFontSet, GetFontSet method [Direct Write], GetFontSet method [Direct Write],IDWriteFontList2 interface, directwrite.idwritefontlist2_getfontset, dwrite_3/IDWriteFontList2::GetFontSet
f1_keywords:
- dwrite_3/IDWriteFontList2.GetFontSet
dev_langs:
- c++
req.construct-type: function
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Dwrite.lib
- Dwrite.dll
api_name:
- IDWriteFontList2::GetFontSet
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

Retrieves the underlying font set used by this list.

## -parameters

### -param fontSet [out]

Type: **[IDWriteFontSet1](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset1)\*\***

The address of a pointer to an [IDWriteFontSet1](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset1) interface. On successful completion, the function sets the pointer to the font set used by the list.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

## -see-also
