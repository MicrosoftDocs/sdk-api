---
UID: NF:dwrite_3.IDWriteFactory7.GetSystemFontSet
title: IDWriteFactory7::GetSystemFontSet
description: Retrieves the set of system fonts. (IDWriteFactory7::GetSystemFontSet)
helpviewer_keywords: ["IDWriteFactory7 interface [Direct Write]","GetSystemFontSet method","IDWriteFactory7.GetSystemFontSet","IDWriteFactory7::GetSystemFontSet","GetSystemFontSet","GetSystemFontSet method [Direct Write]","GetSystemFontSet method [Direct Write]","IDWriteFactory7 interface","directwrite.idwritefactory7_getsystemfontset","dwrite_3/IDWriteFactory7::GetSystemFontSet"]
tech.root: DirectWrite
ms.date: 09/10/2025
ms.keywords: IDWriteFactory7 interface [Direct Write],GetSystemFontSet method, IDWriteFactory7.GetSystemFontSet, IDWriteFactory7::GetSystemFontSet, GetSystemFontSet, GetSystemFontSet method [Direct Write], GetSystemFontSet method [Direct Write],IDWriteFactory7 interface, directwrite.idwritefactory7_getsystemfontset, dwrite_3/IDWriteFactory7::GetSystemFontSet
req.construct-type: function
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 17134
req.target-min-winversvr: Windows 10 Build 17134
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
 - IDWriteFactory7::GetSystemFontSet
 - dwrite_3/IDWriteFactory7::GetSystemFontSet
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
 - IDWriteFactory7::GetSystemFontSet
---

## -description

Retrieves the set of system fonts.

## -parameters

### -param includeDownloadableFonts

Type: **[BOOL](/windows/win32/winprog/windows-data-types)**

`true` if you want to include downloadable fonts. `false` if you only want locally installed fonts.

### -param fontSet

Type: **[IDWriteFontSet2](./nn-dwrite_3-idwritefontset2.md)\*\***

The address of a pointer to an [IDWriteFontSet2](./nn-dwrite_3-idwritefontset2.md) interface. On successful completion, the function sets the pointer to the font set object, otherwise it sets the pointer to `nullptr`.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

## -see-also
