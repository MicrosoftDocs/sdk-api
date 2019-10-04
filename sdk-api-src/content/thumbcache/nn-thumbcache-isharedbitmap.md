---
UID: NN:thumbcache.ISharedBitmap
title: ISharedBitmap (thumbcache.h)
author: windows-sdk-content
description: Exposes memory-efficient methods for accessing bitmaps. This interface is used as a thin wrapper around HBITMAP objects, allowing those objects to be reference counted and protected from having their underlying data changed.
old-location: shell\ISharedBitmap.htm
tech.root: shell
ms.assetid: 72be7757-f969-4f4f-ada1-71789b8d1de0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISharedBitmap, ISharedBitmap interface [Windows Shell], ISharedBitmap interface [Windows Shell],described, _shell_ISharedBitmap, shell.ISharedBitmap, thumbcache/ISharedBitmap
ms.topic: interface
f1_keywords: 
 - "thumbcache/ISharedBitmap"
dev_langs:
 - c++
req.header: thumbcache.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Thumbcache.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Thumbcache.h
api_name:
 - ISharedBitmap
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISharedBitmap interface


## -description


Exposes memory-efficient methods for accessing bitmaps. This interface is used as a thin wrapper around HBITMAP objects, allowing those objects to be reference counted and protected from having their underlying data changed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISharedBitmap</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISharedBitmap</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISharedBitmap</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/thumbcache/nf-thumbcache-isharedbitmap-detach">Detach</a>
</td>
<td align="left" width="63%">
Retrieves the bitmap contained in an <b>ISharedBitmap</b> object, and returns a copy if the contained bitmap resides in shared memory. After calling this method the bitmap is no longer associated with this <b>ISharedBitmap</b> and you cannot call <a href="https://docs.microsoft.com/windows/desktop/api/thumbcache/nf-thumbcache-isharedbitmap-getsharedbitmap">ISharedBitmap::GetSharedBitmap</a> or <a href="https://docs.microsoft.com/windows/desktop/api/thumbcache/nf-thumbcache-isharedbitmap-detach">ISharedBitmap::Detach</a> on it again.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/thumbcache/nf-thumbcache-isharedbitmap-getformat">GetFormat</a>
</td>
<td align="left" width="63%">
Retrieves the alpha type of the bitmap image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/thumbcache/nf-thumbcache-isharedbitmap-getsharedbitmap">GetSharedBitmap</a>
</td>
<td align="left" width="63%">
Retrieves the bitmap contained in an <b>ISharedBitmap</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/thumbcache/nf-thumbcache-isharedbitmap-getsize">GetSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of the bitmap contained in an <b>ISharedBitmap</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/thumbcache/nf-thumbcache-isharedbitmap-initializebitmap">InitializeBitmap</a>
</td>
<td align="left" width="63%">
Initializes a new <b>ISharedBitmap</b> object with a given bitmap.

</td>
</tr>
</table> 


## -remarks



This interface is used in conjunction with the methods of <a href="https://docs.microsoft.com/windows/desktop/api/thumbcache/nn-thumbcache-ithumbnailcache">IThumbnailCache</a>. Bitmaps returned by <a href="https://docs.microsoft.com/windows/desktop/api/thumbcache/nf-thumbcache-ithumbnailcache-getthumbnail">IThumbnailCache::GetThumbnail</a> and <a href="https://docs.microsoft.com/windows/desktop/api/thumbcache/nf-thumbcache-ithumbnailcache-getthumbnailbyid">IThumbnailCache::GetThumbnailByID</a> are of type <b>ISharedBitmap</b>.

When an <b>ISharedBitmap</b> object is retrieved from the thumbnail cache, the underlying bitmap may reside in shared memory to provide improved performance.

The underlying data of the memory-mapped bitmap is protected while the client is accessing it.



