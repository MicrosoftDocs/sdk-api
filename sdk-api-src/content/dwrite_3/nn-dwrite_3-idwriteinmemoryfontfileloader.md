---
UID: NN:dwrite_3.IDWriteInMemoryFontFileLoader
title: IDWriteInMemoryFontFileLoader (dwrite_3.h)
author: windows-sdk-content
description: Represents a font file loader that can access in-memory fonts.
old-location: directwrite\idwriteinmemoryfontfileloader.htm
tech.root: DirectWrite
ms.assetid: E4B2ADAD-E4B8-4655-BABD-F3FC6A3D4F58
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteInMemoryFontFileLoader, IDWriteInMemoryFontFileLoader interface [Direct Write], IDWriteInMemoryFontFileLoader interface [Direct Write],described, directwrite.idwriteinmemoryfontfileloader, dwrite_3/IDWriteInMemoryFontFileLoader
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
ms.custom: 19H1
---

# IDWriteInMemoryFontFileLoader interface


## -description


Represents a font file loader that can access in-memory fonts. 
        The <a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-idwritefactory5-createinmemoryfontfileloader">IDWriteFactory5::CreateInMemoryFontFileLoader</a> method returns an instance of this interface,
        which the client can use to load in-memory fonts without having to implement a custom loader. 
        A client can also create its own custom implementation, however. In either case, the client is responsible for registering and unregistering the loader 
        using <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritefactory-registerfontfileloader">IDWriteFactory::RegisterFontFileLoader</a> 
        and <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritefactory-unregisterfontfileloader">IDWriteFactory::UnregisterFontFileLoader</a>.
      


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteInMemoryFontFileLoader</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritefontfileloader">IDWriteFontFileLoader</a>. <b>IDWriteInMemoryFontFileLoader</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-idwriteinmemoryfontfileloader-createinmemoryfontfilereference">CreateInMemoryFontFileReference</a>
</td>
<td align="left" width="63%">
Creates a font file reference (<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritefontfile">IDWriteFontFile</a> object) from an array of bytes. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/nf-dwrite_3-idwriteinmemoryfontfileloader-getfilecount">GetFileCount</a>
</td>
<td align="left" width="63%">
Returns the number of font file references that have been created using this loader instance.

</td>
</tr>
</table> 


## -see-also




<a href="directwrite.custom_font_sets_win10#creating_a_custom_font_set_using_font_data_loaded_into_memory">Creating a custom font set using font data loaded into memory</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritefontfileloader">IDWriteFontFileLoader</a>
 

 

