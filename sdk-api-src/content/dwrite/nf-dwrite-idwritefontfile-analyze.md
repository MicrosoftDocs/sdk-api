---
UID: NF:dwrite.IDWriteFontFile.Analyze
title: IDWriteFontFile::Analyze
author: windows-sdk-content
description: Analyzes a file and returns whether it represents a font, and whether the font type is supported by the font system.
old-location: directwrite\IDWriteFontFile_Analyze.htm
tech.root: DirectWrite
ms.assetid: 71acbcf8-3024-4e04-ac8e-89cf026b9e91
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Analyze, Analyze method [Direct Write], Analyze method [Direct Write],IDWriteFontFile interface, IDWriteFontFile interface [Direct Write],Analyze method, IDWriteFontFile.Analyze, IDWriteFontFile::Analyze, directwrite.IDWriteFontFile_Analyze, dwrite/IDWriteFontFile::Analyze
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontFile.Analyze
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dwrite.h
: 
- IDWriteFontFile.Analyze
: 
---

# IDWriteFontFile::Analyze


## -description


 Analyzes a file and returns whether it represents a font, and whether the font type is supported by the font system.


## -parameters




### -param isSupportedFontType [out]

Type: <b>BOOL*</b>

<b>TRUE</b> if the font type is supported by the font system; otherwise, <b>FALSE</b>.


### -param fontFileType [out]

Type: <b><a href="https://msdn.microsoft.com/04db41a6-b08b-4d01-a878-c05c0f1f2d9c">DWRITE_FONT_FILE_TYPE</a>*</b>

When this method returns, contains a value that indicates the type of the font file. Note that even if <i> isSupportedFontType</i> is <b>FALSE</b>,
     the <i>fontFileType</i> value may be different from <b>DWRITE_FONT_FILE_TYPE_UNKNOWN</b>.


### -param fontFaceType [out, optional]

Type: <b><a href="https://msdn.microsoft.com/839527fb-2560-4472-8115-960bf5b6badd">DWRITE_FONT_FACE_TYPE</a>*</b>

When this method returns, contains a value that indicates the type of the font face. If <i>fontFileType</i> is not equal to <b>DWRITE_FONT_FILE_TYPE_UNKNOWN</b>, then that can be constructed from the font file.
     


### -param numberOfFaces [out]

Type: <b>UINT32*</b>

When this method returns, contains the number of font faces contained in the font file.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<div class="alert"><b>Important</b>  Certain font file types are recognized, but not supported by the font system.
     For example, the font system will recognize a file as a Type 1 font file
     but will not be able to construct a font face object from it. In such situations, <b>Analyze</b> will set
     <i>isSupportedFontType</i> output parameter to <b>FALSE</b>.
    </div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/d4be5466-0b6c-4cc5-9f16-aa00c6037eb9">IDWriteFontFile</a>
 

 

