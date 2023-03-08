---
UID: NF:oleidl.IOleCache.SetData
title: IOleCache::SetData (oleidl.h)
description: Initializes the cache with data in a specified format and on a specified medium.
helpviewer_keywords: ["IOleCache interface [COM]","SetData method","IOleCache.SetData","IOleCache::SetData","SetData","SetData method [COM]","SetData method [COM]","IOleCache interface","_ole_iolecache_setdata","com.iolecache_setdata","oleidl/IOleCache::SetData"]
old-location: com\iolecache_setdata.htm
tech.root: com
ms.assetid: b826411d-6e00-44ba-8603-85db40c4a55f
ms.date: 12/05/2018
ms.keywords: IOleCache interface [COM],SetData method, IOleCache.SetData, IOleCache::SetData, SetData, SetData method [COM], SetData method [COM],IOleCache interface, _ole_iolecache_setdata, com.iolecache_setdata, oleidl/IOleCache::SetData
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
 - IOleCache::SetData
 - oleidl/IOleCache::SetData
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
 - IOleCache.SetData
---

# IOleCache::SetData


## -description

Initializes the cache with data in a specified format and on a specified medium.

## -parameters

### -param pformatetc [in]

A pointer to a <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structure that specifies the format of the presentation data being placed in the cache.

### -param pmedium [in]

A pointer to a <a href="/windows/win32/api/objidl/ns-objidl-ustgmedium-r1">STGMEDIUM</a> structure that specifies the storage medium that contains the presentation data.

### -param fRelease [in]

Indicates the ownership of the storage medium after completion of the method. If <i>fRelease</i> is <b>TRUE</b>, the cache takes ownership, freeing the medium when it is finished using it. When <i>fRelease</i> is <b>FALSE</b>, the caller retains ownership and is responsible for freeing the medium. The cache can only use the storage medium for the duration of the call.

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
<dt><b>DV_E_LINDEX</b></dt>
</dl>
</td>
<td width="60%">
The value is not valid for <i>pformatetc</i>-&gt;<b>lindex</b>. Currently, only -1 is supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_FORMATETC</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/objidl/ns-objidl-formatetc">FORMATETC</a> structure is invalid.

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
<dt><b>OLE_E_BLANK</b></dt>
</dl>
</td>
<td width="60%">
There is an uninitialized object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_TARGETDEVICE</b></dt>
</dl>
</td>
<td width="60%">
The object is static and <i>pformatetc</i>-&gt;<b>ptd</b> is non-<b>NULL</b>.

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

<b>IOleCache::SetData</b> is usually called when an object is created from the clipboard or through a drag-and-drop operation, and Embed Source data is used to create the object.

<b>IOleCache::SetData</b> and <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache-initcache">IOleCache::InitCache</a> are very similar. There are two main differences. The first difference is that while <b>IOleCache::InitCache</b> initializes the cache with the presentation format provided by the data object, <b>IOleCache::SetData</b> initializes it with a single format. Second, the <b>IOleCache::SetData</b> method ignores the ADVF_NODATA flag while <b>IOleCache::InitCache</b> obeys this flag.

A container can use this method to maintain a single aspect of an object, such as the icon aspect of the object.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-iolecache">IOleCache</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache-cache">IOleCache::Cache</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache-setdata">IOleCache::SetData</a>