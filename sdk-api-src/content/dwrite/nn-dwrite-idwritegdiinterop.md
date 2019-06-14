---
UID: NN:dwrite.IDWriteGdiInterop
title: IDWriteGdiInterop (dwrite.h)
author: windows-sdk-content
description: Provides interoperability with GDI, such as methods to convert a font face to a LOGFONT structure, or to convert a GDI font description into a font face. It is also used to create bitmap render target objects.
old-location: directwrite\IDWriteGdiInterop.htm
tech.root: DirectWrite
ms.assetid: 79472021-ee12-45dd-a943-3908c9e06cde
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteGdiInterop, IDWriteGdiInterop interface [Direct Write], IDWriteGdiInterop interface [Direct Write],described, directwrite.IDWriteGdiInterop, dwrite/IDWriteGdiInterop
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteGdiInterop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteGdiInterop interface


## -description


Provides interoperability with GDI, such as methods to convert a font face to a LOGFONT structure, or to convert a GDI font description into a font face. It is also used to create bitmap render target objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteGdiInterop</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteGdiInterop</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteGdiInterop</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-convertfontfacetologfont">ConvertFontFaceToLOGFONT</a>
</td>
<td align="left" width="63%">
 Initializes a LOGFONT structure based on the GDI-compatible properties of the specified font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-convertfonttologfont">ConvertFontToLOGFONT</a>
</td>
<td align="left" width="63%">
 Initializes a <b>LOGFONT</b> structure based on the GDI-compatible properties of the specified font.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget">CreateBitmapRenderTarget</a>
</td>
<td align="left" width="63%">
 Creates an object that encapsulates a bitmap and memory DC (device context) which can be used for rendering glyphs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc">CreateFontFaceFromHdc</a>
</td>
<td align="left" width="63%">
 Creates an <b>IDWriteFontFace</b> object that corresponds to the currently selected <b>HFONT</b> of the specified <b>HDC</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont">CreateFontFromLOGFONT</a>
</td>
<td align="left" width="63%">
 Creates a font object that matches the properties specified by the <b>LOGFONT</b> structure.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectWrite/interoperating-with-gdi">Interoperating with GDI</a>
 

 

