---
UID: NN:thumbcache.IThumbnailCache
title: IThumbnailCache (thumbcache.h)
author: windows-sdk-content
description: Exposes methods for a system thumbnail cache that is shared across applications.
old-location: shell\IThumbnailCache.htm
tech.root: shell
ms.assetid: b0ddfca0-49b8-4f53-8d22-9a561d09367a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IThumbnailCache, IThumbnailCache interface [Windows Shell], IThumbnailCache interface [Windows Shell],described, _shell_IThumbnailCache, shell.IThumbnailCache, thumbcache/IThumbnailCache
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
 - IThumbnailCache
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IThumbnailCache interface


## -description


Exposes methods for a system thumbnail cache that is shared across applications.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IThumbnailCache</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IThumbnailCache</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IThumbnailCache</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0fcfe68b-5d36-4be1-a468-b5c2d7af0651">GetThumbnail</a>
</td>
<td align="left" width="63%">
Gets a cached thumbnail for a given Shell item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b5069e2-f20b-4c43-a9e7-334366980f5c">GetThumbnailByID</a>
</td>
<td align="left" width="63%">
Gets a thumbnail from the thumbnail cache, given its ID.

</td>
</tr>
</table> 


## -remarks



The Thumbnail Cache API is designed to provide applications with a unified method to retrieve and cache thumbnails. In Windows XP, thumbnail caching is done on a per-folder basis, and the cache is maintained in a Thumbs.db file within each folder. While this approach provides spatial locality, it does not support previews and queries across folders. The thumbnail cache in Windows Vista addresses this shortcoming by providing a global cache.

To cache a thumbnail, an application must first obtain an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> that represents the item for which a thumbnail will be obtained, and then pass the <b>IShellItem</b> to a call to <a href="https://msdn.microsoft.com/0fcfe68b-5d36-4be1-a468-b5c2d7af0651">IThumbnailCache::GetThumbnail</a>. If the flags parameter to <b>IThumbnailCache::GetThumbnail</b> includes the flag WTS_EXTRACT, and the thumbnail is not already cached, a thumbnail will be extracted and placed in the cache. If the flag WTS_FORCEEXTRACTION is set, the cache is ignored and a new thumbnail is always extracted. See the <b>IThumbnailCache::GetThumbnail</b> topic for more details on the flags passed to <b>IThumbnailCache::GetThumbnail</b>.

If a thumbnail is not already in the cache, it will be automatically extracted 
from the source file using the existing implementation(s) of <a href="https://msdn.microsoft.com/28a13749-89e7-407e-89cb-95464859ce3e">IExtractImage</a> or <a href="https://msdn.microsoft.com/55c4739a-4835-4f53-a435-804ddf06ffcf">IThumbnailProvider</a> that is registered on the operating system. Your application does not have to provide an implementation of the thumbnail extractor.

When <a href="https://msdn.microsoft.com/0fcfe68b-5d36-4be1-a468-b5c2d7af0651">IThumbnailCache::GetThumbnail</a> returns, its <i>pThumbnailID</i> parameter receives a WTS_THUMBNAILID structure that contains the unique ID of the thumbnail. If this ID is saved, it can then be passed to <a href="https://msdn.microsoft.com/3b5069e2-f20b-4c43-a9e7-334366980f5c">IThumbnailCache::GetThumbnailByID</a> to retrieve the cached thumbnail. Alternatively, <b>IThumbnailCache::GetThumbnail</b> may be called with the WTS_CACHEONLY flag set. In this case, a thumbnail will be returned only if it is already cached. The disadvantage of using <b>IThumbnailCache::GetThumbnail</b> rather than <b>IThumbnailCache::GetThumbnailByID</b>, is that an <a href="https://msdn.microsoft.com/599b9c0a-df04-4dbd-a5a6-a8736eecc560">IShellItem</a> must still be provided.

Multiple threads can be used to access the thumbnail cache to improve performance.
<a href="https://msdn.microsoft.com/0fcfe68b-5d36-4be1-a468-b5c2d7af0651">IThumbnailCache::GetThumbnail</a> may be called on a higher priority thread with either the WTS_INCACHEONLY or the WTS_FASTEXTRACT flag set, so that cached thumbnails are retrieved immediately. Then if the image is not in the cache, or WTS_LOWQUALITY indicates the cached image was not of ideal quality, a lower priority thread may be used to call <b>IThumbnailCache::GetThumbnail</b> with the WTS_EXTRACT flag set, 
so that a thumbnail may be extracted.



