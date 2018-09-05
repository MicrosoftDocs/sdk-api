---
UID: NF:dwrite_3.IDWriteInMemoryFontFileLoader.CreateInMemoryFontFileReference
title: IDWriteInMemoryFontFileLoader::CreateInMemoryFontFileReference
author: windows-sdk-content
description: Creates a font file reference (IDWriteFontFile object) from an array of bytes.
old-location: directwrite\idwriteinmemoryfontfileloader_createinmemoryfontfilereference.htm
old-project: DirectWrite
ms.assetid: 16570F56-5894-475B-A6AF-6C4BA2C82784
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: CreateInMemoryFontFileReference, CreateInMemoryFontFileReference method [Direct Write], CreateInMemoryFontFileReference method [Direct Write],IDWriteInMemoryFontFileLoader interface, IDWriteInMemoryFontFileLoader interface [Direct Write],CreateInMemoryFontFileReference method, IDWriteInMemoryFontFileLoader.CreateInMemoryFontFileReference, IDWriteInMemoryFontFileLoader::CreateInMemoryFontFileReference, directwrite.idwriteinmemoryfontfileloader_createinmemoryfontfilereference, dwrite_3/IDWriteInMemoryFontFileLoader::CreateInMemoryFontFileReference
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dwrite_3.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
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
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteInMemoryFontFileLoader::CreateInMemoryFontFileReference


## -description


Creates a font file reference (<a href="https://msdn.microsoft.com/d4be5466-0b6c-4cc5-9f16-aa00c6037eb9">IDWriteFontFile</a> object) from an array of bytes. The font file reference is bound to the <a href="https://msdn.microsoft.com/E4B2ADAD-E4B8-4655-BABD-F3FC6A3D4F58">IDWriteInMemoryFontFileLoader</a> instance with which it was
        created and remains valid for as long as that loader is registered with the factory.
      


## -parameters




### -param factory

Type: <b><a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a>*</b>

Factory object used to create the font file reference.


### -param fontData [in]

Type: <b>void const*</b>

Pointer to a memory block containing the font data.


### -param fontDataSize

Type: <b>UINT32</b>

Size of the font data.


### -param ownerObject [in, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680509(v=vs.85).aspx">IUnknown</a>*</b>

Optional object that owns the memory specified by the fontData parameter. If this parameter is not NULL, the method stores a
          pointer to the font data and adds a reference to the owner object. The fontData pointer must remain valid until the owner object is released. If
          this parameter is NULL, the method makes a copy of the font data.


### -param fontFile [out]

Type: <b><a href="https://msdn.microsoft.com/d4be5466-0b6c-4cc5-9f16-aa00c6037eb9">IDWriteFontFile</a>**</b>

Receives a pointer to the newly-created font file reference.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="directwrite.custom_font_sets_win10#creating_a_custom_font_set_using_font_data_loaded_into_memory">Creating a custom font set using font data loaded into memory</a>



<a href="https://msdn.microsoft.com/E4B2ADAD-E4B8-4655-BABD-F3FC6A3D4F58">IDWriteInMemoryFontFileLoader</a>
 

 

