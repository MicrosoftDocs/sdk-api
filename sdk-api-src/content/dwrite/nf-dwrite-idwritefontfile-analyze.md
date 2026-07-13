---
UID: NF:dwrite.IDWriteFontFile.Analyze
title: IDWriteFontFile::Analyze (dwrite.h)
description: Analyzes a file and returns whether it represents a font, and whether the font type is supported by the font system.
helpviewer_keywords: ["Analyze","Analyze method [Direct Write]","Analyze method [Direct Write]","IDWriteFontFile interface","IDWriteFontFile interface [Direct Write]","Analyze method","IDWriteFontFile.Analyze","IDWriteFontFile::Analyze","directwrite.IDWriteFontFile_Analyze","dwrite/IDWriteFontFile::Analyze"]
old-location: directwrite\IDWriteFontFile_Analyze.htm
tech.root: DirectWrite
ms.assetid: 71acbcf8-3024-4e04-ac8e-89cf026b9e91
ms.date: 12/05/2018
ms.keywords: Analyze, Analyze method [Direct Write], Analyze method [Direct Write],IDWriteFontFile interface, IDWriteFontFile interface [Direct Write],Analyze method, IDWriteFontFile.Analyze, IDWriteFontFile::Analyze, directwrite.IDWriteFontFile_Analyze, dwrite/IDWriteFontFile::Analyze
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
 - IDWriteFontFile::Analyze
 - dwrite/IDWriteFontFile::Analyze
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
 - IDWriteFontFile.Analyze
---

# IDWriteFontFile::Analyze


## -description

 Analyzes a file and returns whether it represents a font, and whether the font type is supported by the font system.

## -parameters

### -param isSupportedFontType [out]

Type: <b>BOOL*</b>

<b>TRUE</b> if the font type is supported by the font system; otherwise, <b>FALSE</b>.

### -param fontFileType [out]

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_file_type">DWRITE_FONT_FILE_TYPE</a>*</b>

When this method returns, contains a value that indicates the type of the font file. Note that even if <i> isSupportedFontType</i> is <b>FALSE</b>,
     the <i>fontFileType</i> value may be different from <b>DWRITE_FONT_FILE_TYPE_UNKNOWN</b>.

### -param fontFaceType [out, optional]

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_font_face_type">DWRITE_FONT_FACE_TYPE</a>*</b>

When this method returns, contains a value that indicates the type of the font face. If <i>fontFileType</i> is not equal to <b>DWRITE_FONT_FILE_TYPE_UNKNOWN</b>, then that can be constructed from the font file.

### -param numberOfFaces [out]

Type: <b>UINT32*</b>

When this method returns, contains the number of font faces contained in the font file.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<div class="alert"><b>Important</b>  Certain font file types are recognized, but not supported by the font system.
     For example, the font system will recognize a file as a Type 1 font file
     but will not be able to construct a font face object from it. In such situations, <b>Analyze</b> will set
     <i>isSupportedFontType</i> output parameter to <b>FALSE</b>.
    </div>
<div> </div>

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfile">IDWriteFontFile</a>

