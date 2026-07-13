---
UID: NF:oleidl.IOleCache.Cache
title: IOleCache::Cache (oleidl.h)
description: Specifies the format and other data to be cached inside an embedded object.
helpviewer_keywords: ["Cache","Cache method [COM]","Cache method [COM]","IOleCache interface","IOleCache interface [COM]","Cache method","IOleCache.Cache","IOleCache::Cache","_ole_iolecache_cache","com.iolecache_cache","oleidl/IOleCache::Cache"]
old-location: com\iolecache_cache.htm
tech.root: com
ms.assetid: 2a86063a-3ee6-4fc2-a6e0-6e9ffa658348
ms.date: 12/05/2018
ms.keywords: Cache, Cache method [COM], Cache method [COM],IOleCache interface, IOleCache interface [COM],Cache method, IOleCache.Cache, IOleCache::Cache, _ole_iolecache_cache, com.iolecache_cache, oleidl/IOleCache::Cache
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
 - IOleCache::Cache
 - oleidl/IOleCache::Cache
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
 - IOleCache.Cache
---

# IOleCache::Cache


## -description

Specifies the format and other data to be cached inside an embedded object.

## -parameters

### -param pformatetc [in]

A pointer to a <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structure that specifies the format and other data to be cached. View caching is specified by passing a zero clipboard format in <i>pformatetc</i>.

### -param advf [in]

A group of flags that control the caching. Possible values come from the <a href="/windows/desktop/api/objidl/ne-objidl-advf">ADVF</a> enumeration. When used in this context, for a cache, these values have specific meanings, which are outlined in Remarks. Refer to the <b>ADVF</b> enumeration for a more detailed description.

### -param pdwConnection [out]

A pointer to a variable that receives the identifier of this connection, which can later be used to turn caching off (by passing it to <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache-uncache">IOleCache::Uncache</a>). If this value is 0, the connection was not established. The OLE-provided implementation uses nonzero numbers for connection identifiers.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The supplied <i>pformatetc</i> or <i>advf</i> arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected error has occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory available for the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CACHE_S_FORMATETC_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The cache was created, but the object application does not support the specified format. Cache creation succeeds even if the format is not supported, allowing the caller to fill the cache. If, however, the caller does not need to keep the cache, call <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache-uncache">IOleCache::Uncache</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CACHE_S_SAMECACHE</b></dt>
</dl>
</td>
<td width="60%">
A cache already exists for the <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> passed to <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache-uncache">IOleCache::Uncache</a>. In this case, the new advise flags are assigned to the cache, and the previously assigned connection identifier is returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_LINDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid value for <i>pformatetc</i>-&gt;<b>lindex</b>; currently only -1 is supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_TYMED</b></dt>
</dl>
</td>
<td width="60%">
The value is not valid for <i>pformatetc</i>-&gt;<b>tymed</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_DVASPECT</b></dt>
</dl>
</td>
<td width="60%">
The value is not valid for <i>pformatetc</i>-&gt;<b>dwAspect</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_CLIPFORMAT</b></dt>
</dl>
</td>
<td width="60%">
The value is not valid for <i>pformatetc</i>-&gt;<b>cfFormat</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_NOTINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The cache's storage is not initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_DVTARGETDEVICE</b></dt>
</dl>
</td>
<td width="60%">
The value is not valid for <i>pformatetc-</i>-&gt;<b>ptd</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_STATIC</b></dt>
</dl>
</td>
<td width="60%">
The cache is for a static object and it already has a cache node.

</td>
</tr>
</table>

## -remarks

<b>IOleCache::Cache</b> can specify either data caching or view (presentation) caching. To specify data caching, a valid data format must be passed in <i>pformatetc</i>. For view caching, the cache object itself decides on the format to cache, so a caller would pass a zero data format in <i>pformatetc</i> as follows:


``` syntax
pFormatetc->cfFormat == 0
```

A custom object handler can choose not to store data in a given format. Instead, it can synthesize it on demand when requested.

The <i>advf</i> value specifies a member of the <a href="/windows/desktop/api/objidl/ne-objidl-advf">ADVF</a> enumeration. When one of these values (or an OR'd combination of more than one value) is used in this context, these values mean the following.

<table>
<tr>
<th>ADVF Value</th>
<th>Description</th>
</tr>
<tr>
<td>
ADVF_NODATA

</td>
<td>
The cache is not to be updated by changes made to the running object. Instead, the container will update the cache by explicitly calling <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache-setdata">IOleCache::SetData</a>, <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-setdata">IDataObject::SetData</a>, or <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache2-updatecache">IOleCache2::UpdateCache</a>. This flag is usually used when the iconic aspect of an object is being cached.


</td>
</tr>
<tr>
<td>
ADVF_ONLYONCE

</td>
<td>
Update the cache one time only. After the update is complete, the advisory connection between the object and the cache is disconnected. The source object for the advisory connection calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method.

</td>
</tr>
<tr>
<td>
ADVF_PRIMEFIRST

</td>
<td>
The object is not to wait for the data or view to change before updating the cache. OR'd with ADVF_ONLYONCE, this parameter provides an asynchronous <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a> call.


</td>
</tr>
<tr>
<td>
ADVFCACHE_NOHANDLER

</td>
<td>
Synonym for ADVFCACHE_FORCEBUILTIN.


</td>
</tr>
<tr>
<td>
ADVFCACHE_FORCEBUILTIN

</td>
<td>
Used by DLL object applications and object handlers that draw their objects to cache presentation data to ensure that there is a presentation in the cache. This ensures that the data can be retrieved even when the object or handler code is not available.


</td>
</tr>
<tr>
<td>
ADVFCACHE_ONSAVE

</td>
<td>
Updates the cached representation only when the object containing the cache is saved. The cache is also updated when the OLE object changes from the running state back to the loaded state (because a subsequent save operation would require running the object again).


</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-iolecache">IOleCache</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache-uncache">IOleCache::Uncache</a>
