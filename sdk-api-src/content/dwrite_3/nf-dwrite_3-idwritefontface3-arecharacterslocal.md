---
UID: NF:dwrite_3.IDWriteFontFace3.AreCharactersLocal
title: IDWriteFontFace3::AreCharactersLocal (dwrite_3.h)
description: Determines whether the specified characters are local.
helpviewer_keywords: ["AreCharactersLocal","AreCharactersLocal method [Direct Write]","AreCharactersLocal method [Direct Write]","IDWriteFontFace3 interface","IDWriteFontFace3 interface [Direct Write]","AreCharactersLocal method","IDWriteFontFace3.AreCharactersLocal","IDWriteFontFace3::AreCharactersLocal","directwrite.idwritefontface3_arecharacterslocal","dwrite_3/IDWriteFontFace3::AreCharactersLocal"]
old-location: directwrite\idwritefontface3_arecharacterslocal.htm
tech.root: DirectWrite
ms.assetid: 4cbb6895-3151-c6dd-881e-50d3532c8a14
ms.date: 09/10/2025
ms.keywords: AreCharactersLocal, AreCharactersLocal method [Direct Write], AreCharactersLocal method [Direct Write],IDWriteFontFace3 interface, IDWriteFontFace3 interface [Direct Write],AreCharactersLocal method, IDWriteFontFace3.AreCharactersLocal, IDWriteFontFace3::AreCharactersLocal, directwrite.idwritefontface3_arecharacterslocal, dwrite_3/IDWriteFontFace3::AreCharactersLocal
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IDWriteFontFace3::AreCharactersLocal
 - dwrite_3/IDWriteFontFace3::AreCharactersLocal
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
 - IDWriteFontFace3.AreCharactersLocal
---

# IDWriteFontFace3::AreCharactersLocal


## -description

Determines whether the specified characters are local.

## -parameters

### -param characters [in]

Type: <b>WCHAR</b>

Array of characters.

### -param characterCount

Type: <b>UINT32</b>

The number of elements in the character array.

### -param enqueueIfNotLocal

Type: <b>BOOL</b>

Specifies whether to enqueue a download request    
       if any of the specified characters are not local.

### -param isLocal [out]

Type: <b>BOOL*</b>

Receives TRUE if all of the specified characters are local,    
       FALSE if any of the specified characters are remote.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3">IDWriteFontFace3</a>

