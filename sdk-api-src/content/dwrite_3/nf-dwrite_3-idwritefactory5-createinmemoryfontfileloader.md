---
UID: NF:dwrite_3.IDWriteFactory5.CreateInMemoryFontFileLoader
title: IDWriteFactory5::CreateInMemoryFontFileLoader
author: windows-sdk-content
description: Creates a loader object that can be used to create font file references to in-memory fonts. The caller is responsible for registering and unregistering the loader.
old-location: directwrite\idwritefactory5_createinmemoryfontfileloader.htm
tech.root: DirectWrite
ms.assetid: BA36B91C-C6B8-43B8-BEDA-0089FAE1BAAD
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CreateInMemoryFontFileLoader, CreateInMemoryFontFileLoader method [Direct Write], CreateInMemoryFontFileLoader method [Direct Write],IDWriteFactory5 interface, IDWriteFactory5 interface [Direct Write],CreateInMemoryFontFileLoader method, IDWriteFactory5.CreateInMemoryFontFileLoader, IDWriteFactory5::CreateInMemoryFontFileLoader, directwrite.idwritefactory5_createinmemoryfontfileloader, dwrite_3/IDWriteFactory5::CreateInMemoryFontFileLoader
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite_3.h
req.include-header: 
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
req.lib: Dwrite.lib
req.dll: 
req.irql: 
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory5::CreateInMemoryFontFileLoader


## -description


Creates a loader object that can be used to create font file references to in-memory fonts. The caller is responsible for registering and unregistering the loader.


## -parameters




### -param newLoader [out]

Type: <b><a href="https://msdn.microsoft.com/E4B2ADAD-E4B8-4655-BABD-F3FC6A3D4F58">IDWriteInMemoryFontFileLoader</a>**</b>

Receives a pointer to the newly-created loader object.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns an HRESULT success or error code.




## -see-also




<a href="directwrite.custom_font_sets_win10#creating_a_custom_font_set_using_font_data_loaded_into_memory">Creating a custom font set using font data loaded into memory</a>



<a href="https://msdn.microsoft.com/2F3E30DC-A965-4C68-A337-73F338CF2563">IDWriteFactory5</a>
 

 

