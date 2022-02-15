---
UID: NF:dwrite.IDWriteFactory.GetGdiInterop
title: IDWriteFactory::GetGdiInterop (dwrite.h)
description: Creates an object that is used for interoperability with GDI.
helpviewer_keywords: ["GetGdiInterop","GetGdiInterop method [Direct Write]","GetGdiInterop method [Direct Write]","IDWriteFactory interface","IDWriteFactory interface [Direct Write]","GetGdiInterop method","IDWriteFactory.GetGdiInterop","IDWriteFactory::GetGdiInterop","directwrite.IDWriteFactory_GetGdiInterop","dwrite/IDWriteFactory::GetGdiInterop"]
old-location: directwrite\IDWriteFactory_GetGdiInterop.htm
tech.root: DirectWrite
ms.assetid: 0ff7930b-8840-42d6-b52d-6766deab1aac
ms.date: 12/05/2018
ms.keywords: GetGdiInterop, GetGdiInterop method [Direct Write], GetGdiInterop method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],GetGdiInterop method, IDWriteFactory.GetGdiInterop, IDWriteFactory::GetGdiInterop, directwrite.IDWriteFactory_GetGdiInterop, dwrite/IDWriteFactory::GetGdiInterop
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
 - IDWriteFactory::GetGdiInterop
 - dwrite/IDWriteFactory::GetGdiInterop
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
 - IDWriteFactory.GetGdiInterop
---

# IDWriteFactory::GetGdiInterop


## -description

 Creates an object that is used for interoperability with GDI.

## -parameters

### -param gdiInterop [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop">IDWriteGdiInterop</a>**</b>

When this method returns, contains an address of a pointer to a GDI interop object if successful, or <b>NULL</b> in case of failure.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>

