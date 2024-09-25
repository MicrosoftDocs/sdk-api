---
UID: NF:dwrite_3.IDWriteFontSet1.GetFirstFontResources
title: IDWriteFontSet1::GetFirstFontResources
description: Retrieves a new font set that contains only the first occurrence of each font resource from the set.
helpviewer_keywords: ["IDWriteFontSet1 interface [Direct Write]","GetFirstFontResources method","IDWriteFontSet1.GetFirstFontResources","IDWriteFontSet1::GetFirstFontResources","GetFirstFontResources","GetFirstFontResources method [Direct Write]","GetFirstFontResources method [Direct Write]","IDWriteFontSet1 interface","directwrite.idwritefontset1_getfirstfontresources","dwrite_3/IDWriteFontSet1::GetFirstFontResources"]
tech.root: DirectWrite
ms.date: 09/16/2019
ms.keywords: IDWriteFontSet1 interface [Direct Write],GetFirstFontResources method, IDWriteFontSet1.GetFirstFontResources, IDWriteFontSet1::GetFirstFontResources, GetFirstFontResources, GetFirstFontResources method [Direct Write], GetFirstFontResources method [Direct Write],IDWriteFontSet1 interface, directwrite.idwritefontset1_getfirstfontresources, dwrite_3/IDWriteFontSet1::GetFirstFontResources
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
 - IDWriteFontSet1::GetFirstFontResources
 - dwrite_3/IDWriteFontSet1::GetFirstFontResources
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
 - IDWriteFontSet1::GetFirstFontResources
---

## -description

Retrieves a new font set that contains only the first occurrence of each font resource from the set.

## -parameters

### -param filteredFontSet [out]

Type: **[IDWriteFontSet1](./nn-dwrite_3-idwritefontset1.md)\*\***

The address of a pointer to an [IDWriteFontSet1](./nn-dwrite_3-idwritefontset1.md) interface. On successful completion, the function sets the pointer to a new font set object consisting of single default instances from font resources, otherwise it sets the pointer to `nullptr`.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

## -see-also
