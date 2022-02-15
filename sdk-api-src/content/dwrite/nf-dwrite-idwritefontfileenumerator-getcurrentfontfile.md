---
UID: NF:dwrite.IDWriteFontFileEnumerator.GetCurrentFontFile
title: IDWriteFontFileEnumerator::GetCurrentFontFile (dwrite.h)
description: Gets a reference to the current font file.
helpviewer_keywords: ["GetCurrentFontFile","GetCurrentFontFile method [Direct Write]","GetCurrentFontFile method [Direct Write]","IDWriteFontFileEnumerator interface","IDWriteFontFileEnumerator interface [Direct Write]","GetCurrentFontFile method","IDWriteFontFileEnumerator.GetCurrentFontFile","IDWriteFontFileEnumerator::GetCurrentFontFile","directwrite.IDWriteFontFileEnumerator_GetCurrentFontFile","dwrite/IDWriteFontFileEnumerator::GetCurrentFontFile"]
old-location: directwrite\IDWriteFontFileEnumerator_GetCurrentFontFile.htm
tech.root: DirectWrite
ms.assetid: e541ab2b-2dc8-45df-9d72-8d55141ef142
ms.date: 12/05/2018
ms.keywords: GetCurrentFontFile, GetCurrentFontFile method [Direct Write], GetCurrentFontFile method [Direct Write],IDWriteFontFileEnumerator interface, IDWriteFontFileEnumerator interface [Direct Write],GetCurrentFontFile method, IDWriteFontFileEnumerator.GetCurrentFontFile, IDWriteFontFileEnumerator::GetCurrentFontFile, directwrite.IDWriteFontFileEnumerator_GetCurrentFontFile, dwrite/IDWriteFontFileEnumerator::GetCurrentFontFile
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
 - IDWriteFontFileEnumerator::GetCurrentFontFile
 - dwrite/IDWriteFontFileEnumerator::GetCurrentFontFile
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
 - IDWriteFontFileEnumerator.GetCurrentFontFile
---

# IDWriteFontFileEnumerator::GetCurrentFontFile


## -description

 Gets a reference to the current font file.

## -parameters

### -param fontFile [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfile">IDWriteFontFile</a>**</b>

When this method returns, the address of a pointer to the newly created <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfile">IDWriteFontFile</a>  object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator">IDWriteFontFileEnumerator</a>

