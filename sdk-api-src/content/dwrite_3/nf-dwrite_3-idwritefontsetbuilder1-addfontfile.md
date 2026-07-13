---
UID: NF:dwrite_3.IDWriteFontSetBuilder1.AddFontFile
title: IDWriteFontSetBuilder1::AddFontFile (dwrite_3.h)
description: Adds references to all the fonts in the specified font file.
helpviewer_keywords: ["AddFontFile","AddFontFile method [Direct Write]","AddFontFile method [Direct Write]","IDWriteFontSetBuilder1 interface","IDWriteFontSetBuilder1 interface [Direct Write]","AddFontFile method","IDWriteFontSetBuilder1.AddFontFile","IDWriteFontSetBuilder1::AddFontFile","directwrite.idwritefontsetbuilder1_addfontfile","dwrite_3/IDWriteFontSetBuilder1::AddFontFile"]
old-location: directwrite\idwritefontsetbuilder1_addfontfile.htm
tech.root: DirectWrite
ms.assetid: 3858EF37-F545-4C2E-BC3D-E4732B49911C
ms.date: 09/10/2025
ms.keywords: AddFontFile, AddFontFile method [Direct Write], AddFontFile method [Direct Write],IDWriteFontSetBuilder1 interface, IDWriteFontSetBuilder1 interface [Direct Write],AddFontFile method, IDWriteFontSetBuilder1.AddFontFile, IDWriteFontSetBuilder1::AddFontFile, directwrite.idwritefontsetbuilder1_addfontfile, dwrite_3/IDWriteFontSetBuilder1::AddFontFile
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 14393
req.target-min-winversvr: Windows 10 Build 14393
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
ms.custom: 19H1
f1_keywords:
 - IDWriteFontSetBuilder1::AddFontFile
 - dwrite_3/IDWriteFontSetBuilder1::AddFontFile
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
 - IDWriteFontSetBuilder1.AddFontFile
---

# IDWriteFontSetBuilder1::AddFontFile


## -description

Adds references to all the fonts in the specified font file.  The method parses the font file to determine the fonts and their properties.

## -parameters

### -param fontFile [in]

Type: <b>IDWriteFontFile*</b>

Font file reference object to add to the set. If the file is not a supported OpenType font file, then a DWRITE_E_FILEFORMAT error will be returned.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

[Creating a custom font set using font data loaded into memory](/windows/win32/directwrite/custom-font-sets-win10#creating-a-custom-font-set-using-font-data-loaded-into-memory)

[Creating a font set using arbitrary fonts in the local file system](/windows/win32/directwrite/custom-font-sets-win10#creating-a-font-set-using-arbitrary-fonts-in-the-local-file-system)

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1">IDWriteFontSetBuilder1</a>

