---
UID: NF:dwrite_3.IDWriteFactory6.GetSystemFontSet
title: IDWriteFactory6::GetSystemFontSet
description: Retrieves the set of system fonts.helpviewer_keywords: ["IDWriteFactory6 interface [Direct Write]","GetSystemFontSet method","IDWriteFactory6.GetSystemFontSet","IDWriteFactory6::GetSystemFontSet","GetSystemFontSet","GetSystemFontSet method [Direct Write]","GetSystemFontSet method [Direct Write]","IDWriteFactory6 interface","directwrite.idwritefactory6_getsystemfontset","dwrite_3/IDWriteFactory6::GetSystemFontSet"]
tech.root: DirectWrite
ms.date: 09/12/2019
ms.keywords: IDWriteFactory6 interface [Direct Write],GetSystemFontSet method, IDWriteFactory6.GetSystemFontSet, IDWriteFactory6::GetSystemFontSet, GetSystemFontSet, GetSystemFontSet method [Direct Write], GetSystemFontSet method [Direct Write],IDWriteFactory6 interface, directwrite.idwritefactory6_getsystemfontset, dwrite_3/IDWriteFactory6::GetSystemFontSet
f1_keywords:
- dwrite_3/IDWriteFactory6.GetSystemFontSet
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
- IDWriteFactory6::GetSystemFontSet
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

Retrieves the set of system fonts.

## -parameters

### -param includeDownloadableFonts

Type: **[BOOL](/windows/win32/winprog/windows-data-types)**

`true` if you want to include downloadable fonts. `false` if you only want locally installed fonts.

### -param fontSet

Type: **[IDWriteFontSet1](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset1)\*\***

The address of a pointer to an [IDWriteFontSet1](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset1) interface. On successful completion, the function sets the pointer to the font set object, otherwise it sets the pointer to `nullptr`.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

## -see-also
