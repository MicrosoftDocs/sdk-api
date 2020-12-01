---
UID: NF:oleidl.IOleCache.EnumCache
title: IOleCache::EnumCache (oleidl.h)
description: Creates an enumerator that can be used to enumerate the current cache connections.
helpviewer_keywords: ["EnumCache","EnumCache method [COM]","EnumCache method [COM]","IOleCache interface","IOleCache interface [COM]","EnumCache method","IOleCache.EnumCache","IOleCache::EnumCache","_ole_iolecache_enumcache","com.iolecache_enumcache","oleidl/IOleCache::EnumCache"]
old-location: com\iolecache_enumcache.htm
tech.root: com
ms.assetid: a8d99926-8fb9-4624-8025-483101cb9311
ms.date: 12/05/2018
ms.keywords: EnumCache, EnumCache method [COM], EnumCache method [COM],IOleCache interface, IOleCache interface [COM],EnumCache method, IOleCache.EnumCache, IOleCache::EnumCache, _ole_iolecache_enumcache, com.iolecache_enumcache, oleidl/IOleCache::EnumCache
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
 - IOleCache::EnumCache
 - oleidl/IOleCache::EnumCache
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
 - IOleCache.EnumCache
---

# IOleCache::EnumCache


## -description

Creates an enumerator that can be used to enumerate the current cache connections.

## -parameters

### -param ppenumSTATDATA [out]

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-ienumstatdata">IEnumSTATDATA</a> pointer variable that receives the interface pointer to the new enumerator object. If this parameter is <b>NULL</b>, there are no cache connections at this time.

## -returns

This method returns S_OK if enumerator object is successfully instantiated or there are no cache connections.

<div class="alert"><b>Note</b>  Check the <i>ppenumSTATDATA</i> parameter to determine which result occurred. If the <i>ppenumSTATDATA</i> parameter is <b>NULL</b>, then there are no cache connections at this time.</div>
<div> </div>

## -remarks

The enumerator object returned by this method implements the <a href="/windows/desktop/api/objidl/nn-objidl-ienumstatdata">IEnumSTATDATA</a> interface. <b>IEnumSTATDATA</b> enumerates the data stored in an array of <a href="/windows/desktop/api/objidl/ns-objidl-statdata">STATDATA</a> structures containing information about current cache connections.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ienumstatdata">IEnumSTATDATA</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-iolecache">IOleCache</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache-cache">IOleCache::Cache</a>