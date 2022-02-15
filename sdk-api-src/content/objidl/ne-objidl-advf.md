---
UID: NE:objidl.tagADVF
title: ADVF (objidl.h)
description: Flags that control caching and notification of changes in data.
helpviewer_keywords: ["ADVF","ADVF enumeration [COM]","ADVFCACHE_FORCEBUILTIN","ADVFCACHE_NOHANDLER","ADVFCACHE_ONSAVE","ADVF_DATAONSTOP","ADVF_NODATA","ADVF_ONLYONCE","ADVF_PRIMEFIRST","_ole_ADVF","com.advf","objidl/ADVF","objidl/ADVFCACHE_FORCEBUILTIN","objidl/ADVFCACHE_NOHANDLER","objidl/ADVFCACHE_ONSAVE","objidl/ADVF_DATAONSTOP","objidl/ADVF_NODATA","objidl/ADVF_ONLYONCE","objidl/ADVF_PRIMEFIRST"]
old-location: com\advf.htm
tech.root: com
ms.assetid: e1ad9c17-e492-4891-bf1d-cbac48ce537a
ms.date: 12/05/2018
ms.keywords: ADVF, ADVF enumeration [COM], ADVFCACHE_FORCEBUILTIN, ADVFCACHE_NOHANDLER, ADVFCACHE_ONSAVE, ADVF_DATAONSTOP, ADVF_NODATA, ADVF_ONLYONCE, ADVF_PRIMEFIRST, _ole_ADVF, com.advf, objidl/ADVF, objidl/ADVFCACHE_FORCEBUILTIN, objidl/ADVFCACHE_NOHANDLER, objidl/ADVFCACHE_ONSAVE, objidl/ADVF_DATAONSTOP, objidl/ADVF_NODATA, objidl/ADVF_ONLYONCE, objidl/ADVF_PRIMEFIRST
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ADVF
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagADVF
 - objidl/tagADVF
 - ADVF
 - objidl/ADVF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ObjIdl.h
api_name:
 - ADVF
---

# ADVF enumeration


## -description

Flags that control caching and notification of changes in data.

## -enum-fields

### -field ADVF_NODATA:1

For data advisory connections (<a href="/windows/desktop/api/objidl/nf-objidl-idataobject-dadvise">IDataObject::DAdvise</a> or <a href="/windows/desktop/api/objidl/nf-objidl-idataadviseholder-advise">IDataAdviseHolder::Advise</a>), this flag requests the data object not to send data when it calls <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-ondatachange">IAdviseSink::OnDataChange</a>. The recipient of the change notification can later request the data by calling <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a>. The data object can honor the request by passing TYMED_NULL in the STGMEDIUM parameter, or it can provide the data anyway. For example, the data object might have multiple advisory connections, not all of which specified ADVF_NODATA, in which case the object might send the same notification to all connections. Regardless of the container's request, its <a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a> implementation must check the STGMEDIUM parameter because it is responsible for releasing the medium if it is not TYMED_NULL.

For cache connections (<a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache-cache">IOleCache::Cache</a>), this flag requests that the cache not be updated by changes made to the running object. Instead, the container will update the cache by explicitly calling <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache-setdata">IOleCache::SetData</a>. This situation typically occurs when the iconic aspect of an object is being cached. 

ADVF_NODATA is not a valid flag for view advisory connections (<a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-setadvise">IViewObject::SetAdvise</a>) and it returns E_INVALIDARG.

### -field ADVF_PRIMEFIRST:2

Requests that the object not wait for the data or view to change before making an initial call to <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-ondatachange">IAdviseSink::OnDataChange</a> (for data or view advisory connections) or updating the cache (for cache connections). Used with ADVF_ONLYONCE, this parameter provides an asynchronous <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a> call.

### -field ADVF_ONLYONCE:4

Requests that the object make only one change notification or cache update before deleting the connection. 

ADVF_ONLYONCE automatically deletes the advisory connection after sending one data or view notification. The advisory sink receives only one <a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a> call. A nonzero connection identifier is returned if the connection is established, so the caller can use it to delete the connection prior to the first change notification. 

For data change notifications, the combination of ADVF_ONLYONCE and ADVF_PRIMEFIRST provides, in effect, an asynchronous <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a> call. 

When used with caching, ADVF_ONLYONCE updates the cache one time only, on receipt of the first <a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-ondatachange">IAdviseSink::OnDataChange</a> notification. After the update is complete, the advisory connection between the object and the cache is disconnected. The source object for the advisory connection calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method.

### -field ADVF_DATAONSTOP:64

For data advisory connections, assures accessibility to data. This flag indicates that when the data object is closing, it should call , providing data with the call. Typically, this value is used in combination with ADVF_NODATA. Without th<a href="/windows/desktop/api/objidl/nf-objidl-iadvisesink-ondatachange">IAdviseSink::OnDataChange</a> is value, by the time an <b>OnDataChange</b> call without data reaches the sink, the source might have completed its shutdown and the data might not be accessible. Sinks that specify this value should accept data provided in <b>OnDataChange</b> if it is being passed, because they may not get another chance to retrieve it.

For cache connections, this flag indicates that the object should update the cache as part of object closure.

ADVF_DATAONSTOP is not a valid flag for view advisory connections.

### -field ADVFCACHE_NOHANDLER:8

Synonym for ADVFCACHE_FORCEBUILTIN, which is used more often.

### -field ADVFCACHE_FORCEBUILTIN:16

This value is used by DLL object applications and object handlers that perform the drawing of their objects. ADVFCACHE_FORCEBUILTIN instructs OLE to cache presentation data to ensure that there is a presentation in the cache. This value is not a valid flag for data or view advisory connections. For cache connections, this flag caches data that requires only code shipped with OLE (or the underlying operating system) to be present in order to produce it with <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a> or <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw">IViewObject::Draw</a>. By specifying this value, the container can ensure that the data can be retrieved even when the object or handler code is not available.

### -field ADVFCACHE_ONSAVE:32

For cache connections, this flag updates the cached representation only when the object containing the cache is saved. The cache is also updated when the OLE object transitions from the running state back to the loaded state (because a subsequent save operation would require rerunning the object). This value is not a valid flag for data or view advisory connections.

## -remarks

For a data or view advisory connection, the container uses the <b>ADVF</b> constants when setting up a connection between an <a href="/windows/desktop/api/objidl/nn-objidl-iadvisesink">IAdviseSink</a> instance and either an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> or <a href="/windows/desktop/api/oleidl/nn-oleidl-iviewobject">IViewObject</a> instance. These connections are set up using the <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-dadvise">IDataObject::DAdvise</a>, <a href="/windows/desktop/api/objidl/nf-objidl-idataadviseholder-advise">IDataAdviseHolder::Advise</a>, or <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-setadvise">IViewObject::SetAdvise</a> methods.



For a caching connection, the constants are specified in the <a href="/windows/desktop/api/oleidl/nf-oleidl-iolecache-cache">IOleCache::Cache</a> method to indicate the container's requests on how the object should update its cache.



These constants are also used in the <b>advf</b> member of the <a href="/windows/desktop/api/objidl/ns-objidl-statdata">STATDATA</a> structure. This structure is used by <a href="/windows/desktop/api/objidl/nn-objidl-ienumstatdata">IEnumSTATDATA</a> to describe the enumerated connections, and the <b>advf</b> member indicates the flags that were specified when the advisory or cache connection was established. When <b>STATDATA</b> is used for an<a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-enumadvise"> IOleObject::EnumAdvise</a> enumerator, the <b>advf</b> member is indeterminate.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-idataadviseholder">IDataAdviseHolder</a>



<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ienumstatdata">IEnumSTATDATA</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-iolecache">IOleCache</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-iviewobject">IViewObject</a>
