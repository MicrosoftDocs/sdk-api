---
UID: NF:dwrite_3.IDWriteFactory5.CreateInMemoryFontFileLoader
title: IDWriteFactory5::CreateInMemoryFontFileLoader (dwrite_3.h)
description: Creates a loader object that can be used to create font file references to in-memory fonts. The caller is responsible for registering and unregistering the loader.
helpviewer_keywords: ["CreateInMemoryFontFileLoader","CreateInMemoryFontFileLoader method [Direct Write]","CreateInMemoryFontFileLoader method [Direct Write]","IDWriteFactory5 interface","IDWriteFactory5 interface [Direct Write]","CreateInMemoryFontFileLoader method","IDWriteFactory5.CreateInMemoryFontFileLoader","IDWriteFactory5::CreateInMemoryFontFileLoader","directwrite.idwritefactory5_createinmemoryfontfileloader","dwrite_3/IDWriteFactory5::CreateInMemoryFontFileLoader"]
old-location: directwrite\idwritefactory5_createinmemoryfontfileloader.htm
tech.root: DirectWrite
ms.assetid: BA36B91C-C6B8-43B8-BEDA-0089FAE1BAAD
ms.date: 09/10/2025
ms.keywords: CreateInMemoryFontFileLoader, CreateInMemoryFontFileLoader method [Direct Write], CreateInMemoryFontFileLoader method [Direct Write],IDWriteFactory5 interface, IDWriteFactory5 interface [Direct Write],CreateInMemoryFontFileLoader method, IDWriteFactory5.CreateInMemoryFontFileLoader, IDWriteFactory5::CreateInMemoryFontFileLoader, directwrite.idwritefactory5_createinmemoryfontfileloader, dwrite_3/IDWriteFactory5::CreateInMemoryFontFileLoader
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 15063
req.target-min-winversvr: Windows 10 Build 15063
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
 - IDWriteFactory5::CreateInMemoryFontFileLoader
 - dwrite_3/IDWriteFactory5::CreateInMemoryFontFileLoader
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
 - IDWriteFactory5.CreateInMemoryFontFileLoader
---

# IDWriteFactory5::CreateInMemoryFontFileLoader


## -description

Creates a loader object that can be used to create font file references to in-memory fonts. The caller is responsible for registering and unregistering the loader.

## -parameters

### -param newLoader [out]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader">IDWriteInMemoryFontFileLoader</a>**</b>

Receives a pointer to the newly-created loader object.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

[Creating a custom font set using font data loaded into memory](/windows/win32/directwrite/custom-font-sets-win10#creating-a-custom-font-set-using-font-data-loaded-into-memory)

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5">IDWriteFactory5</a>

