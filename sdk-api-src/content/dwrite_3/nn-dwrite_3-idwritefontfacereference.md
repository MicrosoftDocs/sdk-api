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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontFaceReference interface


## -description


Represents a reference to a font face.
  A uniquely identifying reference to a font, from which you can create a font
  face to query font metrics and use for rendering. A font face reference
  consists of a font file, font face index, and font face simulation. The file
  data may or may not be physically present on the local machine yet.
  


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFontFaceReference</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteFontFaceReference</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f9bc5933-c766-5b30-e2cf-b276a80aecda">CreateFontFace</a>
</td>
<td align="left" width="63%">
Creates a font face from the reference for use with layout, shaping, or rendering.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99b6fb24-2f66-8132-b66e-ca711bb0c7e0">CreateFontFaceWithSimulations</a>
</td>
<td align="left" width="63%">
Creates a font face with alternate font simulations, for example, to explicitly simulate a bold font face out of a regular variant.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ca1b6c7-46c2-2440-35e4-0bcdc375d74e">EnqueueCharacterDownloadRequest</a>
</td>
<td align="left" width="63%">
Adds a request to the font download queue (<a href="https://msdn.microsoft.com/d1b1dfab-a22a-40bb-ffc4-eb094ac14217">IDWriteFontDownloadQueue</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6dfc2793-7960-5c13-950d-9ba14900c3e0">EnqueueFileFragmentDownloadRequest</a>
</td>
<td align="left" width="63%">
Adds a request to the font download queue (<a href="https://msdn.microsoft.com/d1b1dfab-a22a-40bb-ffc4-eb094ac14217">IDWriteFontDownloadQueue</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94b1adb2-42d5-bdfa-ce99-52e67e0f7cf5">EnqueueFontDownloadRequest</a>
</td>
<td align="left" width="63%">
Adds a request to the font download queue (<a href="https://msdn.microsoft.com/d1b1dfab-a22a-40bb-ffc4-eb094ac14217">IDWriteFontDownloadQueue</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e35c011-8d5b-0bb5-fea2-4034b8e379aa">EnqueueGlyphDownloadRequest</a>
</td>
<td align="left" width="63%">
Adds a request to the font download queue (<a href="https://msdn.microsoft.com/d1b1dfab-a22a-40bb-ffc4-eb094ac14217">IDWriteFontDownloadQueue</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7988e724-2ccb-b182-8262-dacee1aa1f96">GetFileSize</a>
</td>
<td align="left" width="63%">
Get the total size of the font face in bytes.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98de8a3d-073e-78df-2e2c-8ab64632091c">GetFileTime</a>
</td>
<td align="left" width="63%">
Get the last modified date.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/963ec564-8a7e-5916-f630-844bd37af051">GetFontFaceIndex</a>
</td>
<td align="left" width="63%">
Obtains the zero-based index of the font face in its font file or files. If the font files contain a single face,  
   the return value is zero. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ceef760-32af-5b55-62ca-88adcc23696f">GetFontFile</a>
</td>
<td align="left" width="63%">
Obtains the font file representing a font face.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f6dc5cf5-131f-a451-7979-3ae8613577bb">GetLocalFileSize</a>
</td>
<td align="left" width="63%">
Get the local size of the font face in bytes, which will always be   
   less than or equal to GetFullSize. If the locality is remote, this     
   value is zero. If full, this value will equal GetFileSize.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/533f30a7-bf54-670e-63be-ffb9b07fb9d8">GetLocality</a>
</td>
<td align="left" width="63%">
Get the locality of this font face reference.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/537e7a1a-894b-a569-b365-1d563a46eca7">GetSimulations</a>
</td>
<td align="left" width="63%">
Obtains the algorithmic style simulation flags of a font face.

</td>
</tr>
</table> 

