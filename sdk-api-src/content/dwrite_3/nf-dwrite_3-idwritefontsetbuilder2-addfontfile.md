---
UID: NF:dwrite_3.IDWriteFontSetBuilder2.AddFontFile
title: IDWriteFontSetBuilder2::AddFontFile
description: Adds references to all the fonts in the specified font file. The method parses the font file to determine the fonts and their properties.
helpviewer_keywords: ["IDWriteFontSetBuilder2 interface [Direct Write]","AddFontFile method","IDWriteFontSetBuilder2.AddFontFile","IDWriteFontSetBuilder2::AddFontFile","AddFontFile","AddFontFile method [Direct Write]","AddFontFile method [Direct Write]","IDWriteFontSetBuilder2 interface","directwrite.idwritefontsetbuilder2_addfontfile","dwrite_3/IDWriteFontSetBuilder2::AddFontFile"]
tech.root: DirectWrite
ms.date: 09/10/2025
ms.keywords: IDWriteFontSetBuilder2 interface [Direct Write],AddFontFile method, IDWriteFontSetBuilder2.AddFontFile, IDWriteFontSetBuilder2::AddFontFile, AddFontFile, AddFontFile method [Direct Write], AddFontFile method [Direct Write],IDWriteFontSetBuilder2 interface, directwrite.idwritefontsetbuilder2_addfontfile, dwrite_3/IDWriteFontSetBuilder2::AddFontFile
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
 - IDWriteFontSetBuilder2::AddFontFile
 - dwrite_3/IDWriteFontSetBuilder2::AddFontFile
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
 - IDWriteFontSetBuilder2::AddFontFile
---

## -description

Adds references to all the fonts in the specified font file. The method parses the font file to determine the fonts and their properties.

## -parameters

### -param filePath

Type: **[WCHAR](/windows/win32/winprog/windows-data-types) const \***

Absolute file path to add to the font set.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

## -see-also

