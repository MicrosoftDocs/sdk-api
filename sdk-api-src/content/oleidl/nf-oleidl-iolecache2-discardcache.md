---
UID: NF:oleidl.IOleCache2.DiscardCache
title: IOleCache2::DiscardCache (oleidl.h)
author: windows-sdk-content
description: Discards the caches found in memory.
old-location: com\iolecache2_discardcache.htm
tech.root: com
ms.assetid: 03fb4bdb-1655-4923-b124-8854419766ec
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DiscardCache, DiscardCache method [COM], DiscardCache method [COM],IOleCache2 interface, IOleCache2 interface [COM],DiscardCache method, IOleCache2.DiscardCache, IOleCache2::DiscardCache, _ole_iolecache2_discardcache, com.iolecache2_discardcache, oleidl/IOleCache2::DiscardCache
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - OleIdl.h
api_name:
 - IOleCache2.DiscardCache
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOleCache2::DiscardCache


## -description


Discards the caches found in memory.


## -parameters




### -param dwDiscardOptions [in]

A value from the <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/ne-oleidl-tagdiscardcache">DISCARDCACHE</a> enumeration that indicates whether data is to be saved prior to being discarded. Containers that have drawn a large object and need to free up memory can specify DISCARDCACHE_SAVEIFDIRTY so that the newest presentation is saved for the next time the object must be drawn.

Containers that have activated an embedded object, made some changes, and then called <a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nf-oleidl-ioleobject-close">IOleObject::Close</a> with OLECLOSE_NOSAVE to roll back the changes can specify DISCARDCACHE_NOSAVE to ensure that the native and presentation data are not out of synchronization.


## -returns



This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_NOSTORAGE</b></dt>
</dl>
</td>
<td width="60%">
There is no storage available for saving the data in the cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_MEDIUMFULL</b></dt>
</dl>
</td>
<td width="60%">
The storage medium is full.

</td>
</tr>
</table>
 




## -remarks



The <b>IOleCache2::DiscardCache</b> method is commonly used to handle low memory conditions by freeing memory currently being used by presentation caches.

After it is discarded, a cache will satisfy subsequent <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a> calls by reverting to disk-based data.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolecache">IOleCache</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolecache2">IOleCache2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/oleidl/nn-oleidl-iolecachecontrol">IOleCacheControl</a>
 

 

