---
UID: NF:dwrite_3.IDWriteInMemoryFontFileLoader.CreateInMemoryFontFileReference
title: IDWriteInMemoryFontFileLoader::CreateInMemoryFontFileReference (dwrite_3.h)
description: Creates a font file reference (IDWriteFontFile object) from an array of bytes.
helpviewer_keywords: ["CreateInMemoryFontFileReference","CreateInMemoryFontFileReference method [Direct Write]","CreateInMemoryFontFileReference method [Direct Write]","IDWriteInMemoryFontFileLoader interface","IDWriteInMemoryFontFileLoader interface [Direct Write]","CreateInMemoryFontFileReference method","IDWriteInMemoryFontFileLoader.CreateInMemoryFontFileReference","IDWriteInMemoryFontFileLoader::CreateInMemoryFontFileReference","directwrite.idwriteinmemoryfontfileloader_createinmemoryfontfilereference","dwrite_3/IDWriteInMemoryFontFileLoader::CreateInMemoryFontFileReference"]
old-location: directwrite\idwriteinmemoryfontfileloader_createinmemoryfontfilereference.htm
tech.root: DirectWrite
ms.assetid: 16570F56-5894-475B-A6AF-6C4BA2C82784
ms.date: 09/10/2025
ms.keywords: CreateInMemoryFontFileReference, CreateInMemoryFontFileReference method [Direct Write], CreateInMemoryFontFileReference method [Direct Write],IDWriteInMemoryFontFileLoader interface, IDWriteInMemoryFontFileLoader interface [Direct Write],CreateInMemoryFontFileReference method, IDWriteInMemoryFontFileLoader.CreateInMemoryFontFileReference, IDWriteInMemoryFontFileLoader::CreateInMemoryFontFileReference, directwrite.idwriteinmemoryfontfileloader_createinmemoryfontfilereference, dwrite_3/IDWriteInMemoryFontFileLoader::CreateInMemoryFontFileReference
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
 - IDWriteInMemoryFontFileLoader::CreateInMemoryFontFileReference
 - dwrite_3/IDWriteInMemoryFontFileLoader::CreateInMemoryFontFileReference
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
 - IDWriteInMemoryFontFileLoader.CreateInMemoryFontFileReference
---

# IDWriteInMemoryFontFileLoader::CreateInMemoryFontFileReference


## -description

Creates a font file reference (<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfile">IDWriteFontFile</a> object) from an array of bytes. The font file reference is bound to the <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader">IDWriteInMemoryFontFileLoader</a> instance with which it was
        created and remains valid for as long as that loader is registered with the factory.

## -parameters

### -param factory

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>*</b>

Factory object used to create the font file reference.

### -param fontData [in]

Type: <b>void const*</b>

Pointer to a memory block containing the font data.

### -param fontDataSize

Type: <b>UINT32</b>

Size of the font data.

### -param ownerObject [in, optional]

Type: <b><a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

Optional object that owns the memory specified by the fontData parameter. If this parameter is not NULL, the method stores a
          pointer to the font data and adds a reference to the owner object. The fontData pointer must remain valid until the owner object is released. If
          this parameter is NULL, the method makes a copy of the font data.

### -param fontFile [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfile">IDWriteFontFile</a>**</b>

Receives a pointer to the newly-created font file reference.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns an HRESULT success or error code.

## -see-also

[Creating a custom font set using font data loaded into memory](/windows/win32/directwrite/custom-font-sets-win10#creating-a-custom-font-set-using-font-data-loaded-into-memory)

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader">IDWriteInMemoryFontFileLoader</a>

