---
UID: NN:thumbcache.ISharedBitmap
title: ISharedBitmap
author: windows-sdk-content
description: Exposes memory-efficient methods for accessing bitmaps. This interface is used as a thin wrapper around HBITMAP objects, allowing those objects to be reference counted and protected from having their underlying data changed.
old-location: shell\ISharedBitmap.htm
tech.root: shell
ms.assetid: 72be7757-f969-4f4f-ada1-71789b8d1de0
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ISharedBitmap, ISharedBitmap interface [Windows Shell], ISharedBitmap interface [Windows Shell],described, _shell_ISharedBitmap, shell.ISharedBitmap, thumbcache/ISharedBitmap
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISharedBitmap interface


## -description


Exposes memory-efficient methods for accessing bitmaps. This interface is used as a thin wrapper around HBITMAP objects, allowing those objects to be reference counted and protected from having their underlying data changed.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISharedBitmap</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISharedBitmap</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/1d68beca-c254-435e-a1cd-04e7aa462c84">Detach</a>
</td>
<td align="left" width="63%">
Retrieves the bitmap contained in an <b>ISharedBitmap</b> object, and returns a copy if the contained bitmap resides in shared memory. After calling this method the bitmap is no longer associated with this <b>ISharedBitmap</b> and you cannot call <a href="https://msdn.microsoft.com/0d2cfdba-b51f-4035-b0b2-e48933505c73">ISharedBitmap::GetSharedBitmap</a> or <a href="https://msdn.microsoft.com/1d68beca-c254-435e-a1cd-04e7aa462c84">ISharedBitmap::Detach</a> on it again.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/403b8b19-c96f-4205-999f-103025d2b923">GetFormat</a>
</td>
<td align="left" width="63%">
Retrieves the alpha type of the bitmap image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d2cfdba-b51f-4035-b0b2-e48933505c73">GetSharedBitmap</a>
</td>
<td align="left" width="63%">
Retrieves the bitmap contained in an <b>ISharedBitmap</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/612fbb6d-2539-4055-9037-7e64ddced4e9">GetSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of the bitmap contained in an <b>ISharedBitmap</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55018484-df70-43fa-b494-215035b90ceb">InitializeBitmap</a>
</td>
<td align="left" width="63%">
Initializes a new <b>ISharedBitmap</b> object with a given bitmap.

</td>
</tr>
</table> 


## -remarks



This interface is used in conjunction with the methods of <a href="https://msdn.microsoft.com/b0ddfca0-49b8-4f53-8d22-9a561d09367a">IThumbnailCache</a>. Bitmaps returned by <a href="https://msdn.microsoft.com/0fcfe68b-5d36-4be1-a468-b5c2d7af0651">IThumbnailCache::GetThumbnail</a> and <a href="https://msdn.microsoft.com/3b5069e2-f20b-4c43-a9e7-334366980f5c">IThumbnailCache::GetThumbnailByID</a> are of type <b>ISharedBitmap</b>.

When an <b>ISharedBitmap</b> object is retrieved from the thumbnail cache, the underlying bitmap may reside in shared memory to provide improved performance.

The underlying data of the memory-mapped bitmap is protected while the client is accessing it.



