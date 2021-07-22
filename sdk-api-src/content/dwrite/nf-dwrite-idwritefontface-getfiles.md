---
UID: NF:dwrite.IDWriteFontFace.GetFiles
title: IDWriteFontFace::GetFiles (dwrite.h)
description: Obtains the font files representing a font face.
helpviewer_keywords: ["GetFiles","GetFiles method [Direct Write]","GetFiles method [Direct Write]","IDWriteFontFace interface","IDWriteFontFace interface [Direct Write]","GetFiles method","IDWriteFontFace.GetFiles","IDWriteFontFace::GetFiles","directwrite.IDWriteFontFace_GetFiles","dwrite/IDWriteFontFace::GetFiles"]
old-location: directwrite\IDWriteFontFace_GetFiles.htm
tech.root: DirectWrite
ms.assetid: 505238e5-bfc9-4d5e-b807-3c5e8b2e82d3
ms.date: 12/05/2018
ms.keywords: GetFiles, GetFiles method [Direct Write], GetFiles method [Direct Write],IDWriteFontFace interface, IDWriteFontFace interface [Direct Write],GetFiles method, IDWriteFontFace.GetFiles, IDWriteFontFace::GetFiles, directwrite.IDWriteFontFace_GetFiles, dwrite/IDWriteFontFace::GetFiles
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
 - IDWriteFontFace::GetFiles
 - dwrite/IDWriteFontFace::GetFiles
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
 - IDWriteFontFace.GetFiles
---

# IDWriteFontFace::GetFiles


## -description

 Obtains the font files representing a font face.

## -parameters

### -param numberOfFiles [in, out]

Type: <b>UINT32*</b>

If <i>fontFiles</i> is <b>NULL</b>, receives the number of files representing the font face.  Otherwise, the number of font files being requested should be passed.  See the Remarks section below for more information.

### -param fontFiles [out, optional]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfile">IDWriteFontFile</a>**</b>

When this method returns, contains a pointer to a user-provided array that stores pointers to font files representing the font face.
     This parameter can be <b>NULL</b> if the user wants only the number of files representing the font face.
     This API increments reference count of the font file pointers returned according to COM conventions, and the client
     should release them when finished.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>IDWriteFontFace::GetFiles</b> method should be called twice.  The first time you call <b>GetFiles</b><i>fontFiles</i> should be <b>NULL</b>. When the method returns, <i>numberOfFiles</i> receives the number of font files that represent the font face.

Then, call the method a second time, passing the <i>numberOfFiles</i> value that was output the first call, and a non-null buffer of the correct size to store the <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfile">IDWriteFontFile</a> pointers.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontface">IDWriteFontFace</a>

