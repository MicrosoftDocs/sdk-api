---
UID: NN:dwrite_3.IDWriteGdiInterop1
title: IDWriteGdiInterop1
author: windows-sdk-content
description: Provides interoperability with GDI, such as methods to convert a font face to a LOGFONT structure, or to convert a GDI font description into a font face. It is also used to create bitmap render target objects.
old-location: directwrite\idwritegdiinterop1.htm
tech.root: DirectWrite
ms.assetid: A69922D8-EF9F-4F46-91D3-F7F649CF4705
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IDWriteGdiInterop1, IDWriteGdiInterop1 interface [Direct Write], IDWriteGdiInterop1 interface [Direct Write],described, directwrite.idwritegdiinterop1, dwrite_3/IDWriteGdiInterop1
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
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteGdiInterop1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteGdiInterop1 interface


## -description


Provides interoperability with GDI, such as methods to convert a font face to a LOGFONT structure, or to convert a GDI font description into a font face. 
        It is also used to create bitmap render target objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteGdiInterop1</b> interface inherits from <a href="https://msdn.microsoft.com/79472021-ee12-45dd-a943-3908c9e06cde">IDWriteGdiInterop</a>. <b>IDWriteGdiInterop1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteGdiInterop1</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AA28755A-C2E3-4177-A5DD-61D9809A9D0E">CreateFontFromLOGFONT</a>
</td>
<td align="left" width="63%">
Creates a font object that matches the properties specified by the LOGFONT structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83967afd-8309-74b7-da76-1caee04a4990">GetFontSignature</a>
</td>
<td align="left" width="63%">Overloaded. Retrieves a font signature.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38D547D2-0C1C-4673-83BD-38458DFD7E5A">GetMatchingFontsByLOGFONT</a>
</td>
<td align="left" width="63%">
Gets a list of matching fonts based on the specified LOGFONT values. Only fonts
        of that family name will be returned.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/79472021-ee12-45dd-a943-3908c9e06cde">IDWriteGdiInterop</a>
 

 

