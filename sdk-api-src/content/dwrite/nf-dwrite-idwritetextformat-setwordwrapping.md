---
UID: NF:dwrite.IDWriteTextFormat.SetWordWrapping
title: IDWriteTextFormat::SetWordWrapping (dwrite.h)
description: Sets the word wrapping option.
helpviewer_keywords: ["IDWriteTextFormat interface [Direct Write]","SetWordWrapping method","IDWriteTextFormat.SetWordWrapping","IDWriteTextFormat::SetWordWrapping","SetWordWrapping","SetWordWrapping method [Direct Write]","SetWordWrapping method [Direct Write]","IDWriteTextFormat interface","directwrite.IDWriteTextFormat_SetWordWrapping","dwrite/IDWriteTextFormat::SetWordWrapping"]
old-location: directwrite\IDWriteTextFormat_SetWordWrapping.htm
tech.root: DirectWrite
ms.assetid: 04c9fc62-d5a3-470b-bcae-4c6570eebdaa
ms.date: 12/05/2018
ms.keywords: IDWriteTextFormat interface [Direct Write],SetWordWrapping method, IDWriteTextFormat.SetWordWrapping, IDWriteTextFormat::SetWordWrapping, SetWordWrapping, SetWordWrapping method [Direct Write], SetWordWrapping method [Direct Write],IDWriteTextFormat interface, directwrite.IDWriteTextFormat_SetWordWrapping, dwrite/IDWriteTextFormat::SetWordWrapping
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
 - IDWriteTextFormat::SetWordWrapping
 - dwrite/IDWriteTextFormat::SetWordWrapping
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
 - IDWriteTextFormat.SetWordWrapping
---

# IDWriteTextFormat::SetWordWrapping


## -description

 Sets the word wrapping option.

## -parameters

### -param wordWrapping

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_word_wrapping">DWRITE_WORD_WRAPPING</a></b>

The word wrapping option being set for a paragraph; see <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_word_wrapping">DWRITE_WORD_WRAPPING</a> for more information.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a>

