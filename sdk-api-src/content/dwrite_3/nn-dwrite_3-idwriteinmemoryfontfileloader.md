---
UID: NN:dwrite_3.IDWriteInMemoryFontFileLoader
title: IDWriteInMemoryFontFileLoader
author: windows-sdk-content
description: Represents a font file loader that can access in-memory fonts.
old-location: directwrite\idwriteinmemoryfontfileloader.htm
tech.root: DirectWrite
ms.assetid: E4B2ADAD-E4B8-4655-BABD-F3FC6A3D4F58
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IDWriteInMemoryFontFileLoader, IDWriteInMemoryFontFileLoader interface [Direct Write], IDWriteInMemoryFontFileLoader interface [Direct Write],described, directwrite.idwriteinmemoryfontfileloader, dwrite_3/IDWriteInMemoryFontFileLoader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IDWriteInMemoryFontFileLoader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteInMemoryFontFileLoader interface


## -description


Represents a font file loader that can access in-memory fonts. 
        The <a href="https://msdn.microsoft.com/BA36B91C-C6B8-43B8-BEDA-0089FAE1BAAD">IDWriteFactory5::CreateInMemoryFontFileLoader</a> method returns an instance of this interface,
        which the client can use to load in-memory fonts without having to implement a custom loader. 
        A client can also create its own custom implementation, however. In either case, the client is responsible for registering and unregistering the loader 
        using <a href="https://msdn.microsoft.com/f5b28c3d-c3ad-4435-92c8-07841e8d160a">IDWriteFactory::RegisterFontFileLoader</a> 
        and <a href="https://msdn.microsoft.com/f048671e-dfb6-449d-9bcd-e5df8408c01a">IDWriteFactory::UnregisterFontFileLoader</a>.
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteInMemoryFontFileLoader</b> interface inherits from <a href="https://msdn.microsoft.com/855e281e-3855-4c11-af87-68f8e0dadbf8">IDWriteFontFileLoader</a>. <b>IDWriteInMemoryFontFileLoader</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteInMemoryFontFileLoader</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/16570F56-5894-475B-A6AF-6C4BA2C82784">CreateInMemoryFontFileReference</a>
</td>
<td align="left" width="63%">
Creates a font file reference (<a href="https://msdn.microsoft.com/d4be5466-0b6c-4cc5-9f16-aa00c6037eb9">IDWriteFontFile</a> object) from an array of bytes. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02385843-FDE6-408A-BD48-BBDC7DE4CA67">GetFileCount</a>
</td>
<td align="left" width="63%">
Returns the number of font file references that have been created using this loader instance.

</td>
</tr>
</table> 


## -see-also




<a href="directwrite.custom_font_sets_win10#creating_a_custom_font_set_using_font_data_loaded_into_memory">Creating a custom font set using font data loaded into memory</a>



<a href="https://msdn.microsoft.com/855e281e-3855-4c11-af87-68f8e0dadbf8">IDWriteFontFileLoader</a>
 

 

