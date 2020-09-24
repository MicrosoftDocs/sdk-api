---
UID: NF:oleidl.IOleCache.Uncache
title: IOleCache::Uncache (oleidl.h)
description: Removes a cache connection created previously using IOleCache::Cache.
helpviewer_keywords: ["IOleCache interface [COM]","Uncache method","IOleCache.Uncache","IOleCache::Uncache","Uncache","Uncache method [COM]","Uncache method [COM]","IOleCache interface","_ole_iolecache_uncache","com.iolecache_uncache","oleidl/IOleCache::Uncache"]
old-location: com\iolecache_uncache.htm
tech.root: com
ms.assetid: a6a57bdd-190f-485b-9b46-cbfc1a1d29a6
ms.date: 12/05/2018
ms.keywords: IOleCache interface [COM],Uncache method, IOleCache.Uncache, IOleCache::Uncache, Uncache, Uncache method [COM], Uncache method [COM],IOleCache interface, _ole_iolecache_uncache, com.iolecache_uncache, oleidl/IOleCache::Uncache
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOleCache::Uncache
 - oleidl/IOleCache::Uncache
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IOleCache.Uncache
---

# IOleCache::Uncache


## -description

Removes a cache connection created previously using <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache-cache">IOleCache::Cache</a>.

## -parameters

### -param dwConnection [in]

The cache connection to be removed. This nonzero value was returned by <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache-cache">IOleCache::Cache</a> when the cache was originally established.

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
<dt><b>OLE_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
No cache connection exists for <i>dwConnection</i>.

</td>
</tr>
</table>

## -remarks

The <b>IOleCache::Uncache</b> method removes a cache connection that was created in a prior call to <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache-cache">IOleCache::Cache</a>. It uses the <i>dwConnection</i> parameter that was returned by the prior call to <b>IOleCache::Cache</b>.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-iolecache">IOleCache</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache-cache">IOleCache::Cache</a>