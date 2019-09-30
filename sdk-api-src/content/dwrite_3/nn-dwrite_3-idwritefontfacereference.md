---
UID: NN:dwrite_3.IDWriteFontFaceReference
title: IDWriteFontFaceReference (dwrite_3.h)
author: windows-sdk-content
description: Represents a reference to a font face.
old-location: directwrite\idwritefontfacereference.htm
tech.root: DirectWrite
ms.assetid: 04242508-7439-43B6-B3E7-07617B782038
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteFontFaceReference, IDWriteFontFaceReference interface [Direct Write], IDWriteFontFaceReference interface [Direct Write],described, directwrite.idwritefontfacereference, dwrite_3/IDWriteFontFaceReference
ms.topic: interface
f1_keywords: 
 - "dwrite_3/IDWriteFontFaceReference"
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - IDWriteFontFaceReference
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFontFaceReference interface


## -description


Represents a reference to a font face.
  A uniquely identifying reference to a font, from which you can create a font
  face to query font metrics and use for rendering. A font face reference
  consists of a font file, font face index, and font face simulation. The file
  data may or may not be physically present on the local machine yet.
  


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFontFaceReference</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteFontFaceReference</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFontFaceReference</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-createfontface">CreateFontFace</a>
</td>
<td align="left" width="63%">
Creates a font face from the reference for use with layout, shaping, or rendering.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-createfontfacewithsimulations">CreateFontFaceWithSimulations</a>
</td>
<td align="left" width="63%">
Creates a font face with alternate font simulations, for example, to explicitly simulate a bold font face out of a regular variant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuecharacterdownloadrequest">EnqueueCharacterDownloadRequest</a>
</td>
<td align="left" width="63%">
Adds a request to the font download queue (<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue">IDWriteFontDownloadQueue</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuefilefragmentdownloadrequest">EnqueueFileFragmentDownloadRequest</a>
</td>
<td align="left" width="63%">
Adds a request to the font download queue (<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue">IDWriteFontDownloadQueue</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuefontdownloadrequest">EnqueueFontDownloadRequest</a>
</td>
<td align="left" width="63%">
Adds a request to the font download queue (<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue">IDWriteFontDownloadQueue</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueueglyphdownloadrequest">EnqueueGlyphDownloadRequest</a>
</td>
<td align="left" width="63%">
Adds a request to the font download queue (<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue">IDWriteFontDownloadQueue</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-getfilesize">GetFileSize</a>
</td>
<td align="left" width="63%">
Get the total size of the font face in bytes.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-getfiletime">GetFileTime</a>
</td>
<td align="left" width="63%">
Get the last modified date.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-getfontfaceindex">GetFontFaceIndex</a>
</td>
<td align="left" width="63%">
Obtains the zero-based index of the font face in its font file or files. If the font files contain a single face,  
   the return value is zero. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-getfontfile">GetFontFile</a>
</td>
<td align="left" width="63%">
Obtains the font file representing a font face.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-getlocalfilesize">GetLocalFileSize</a>
</td>
<td align="left" width="63%">
Get the local size of the font face in bytes, which will always be   
   less than or equal to GetFullSize. If the locality is remote, this     
   value is zero. If full, this value will equal GetFileSize.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-getlocality">GetLocality</a>
</td>
<td align="left" width="63%">
Get the locality of this font face reference.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-getsimulations">GetSimulations</a>
</td>
<td align="left" width="63%">
Obtains the algorithmic style simulation flags of a font face.

</td>
</tr>
</table> 

