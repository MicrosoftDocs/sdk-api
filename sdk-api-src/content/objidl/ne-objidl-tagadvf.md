---
UID: NE:objidl.tagADVF
title: tagADVF
author: windows-sdk-content
description: Flags that control caching and notification of changes in data.
old-location: com\advf.htm
old-project: com
ms.assetid: e1ad9c17-e492-4891-bf1d-cbac48ce537a
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: ADVF, ADVF enumeration [COM], ADVFCACHE_FORCEBUILTIN, ADVFCACHE_NOHANDLER, ADVFCACHE_ONSAVE, ADVF_DATAONSTOP, ADVF_NODATA, ADVF_ONLYONCE, ADVF_PRIMEFIRST, _ole_ADVF, com.advf, objidl/ADVF, objidl/ADVFCACHE_FORCEBUILTIN, objidl/ADVFCACHE_NOHANDLER, objidl/ADVFCACHE_ONSAVE, objidl/ADVF_DATAONSTOP, objidl/ADVF_NODATA, objidl/ADVF_ONLYONCE, objidl/ADVF_PRIMEFIRST, tagADVF
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidlbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ADVF
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ObjIdl.h
api_name:
-	ADVF
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# tagADVF enumeration


## -description


Flags that control caching and notification of changes in data.


## -enum-fields




### -field ADVF_NODATA

For data advisory connections (<a href="https://msdn.microsoft.com/be9891d4-aad3-42a0-8c8e-4b86091ff03b">IDataObject::DAdvise</a> or <a href="https://msdn.microsoft.com/3b72a50b-a18f-4ec0-9d1d-52b07eb84faf">IDataAdviseHolder::Advise</a>), this flag requests the data object not to send data when it calls <a href="https://msdn.microsoft.com/834a5328-3a1f-4edb-aad0-be8ab87acb04">IAdviseSink::OnDataChange</a>. The recipient of the change notification can later request the data by calling <a href="https://msdn.microsoft.com/05118461-0438-4715-b2c2-fc2471ce38f0">IDataObject::GetData</a>. The data object can honor the request by passing TYMED_NULL in the STGMEDIUM parameter, or it can provide the data anyway. For example, the data object might have multiple advisory connections, not all of which specified ADVF_NODATA, in which case the object might send the same notification to all connections. Regardless of the container's request, its <a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a> implementation must check the STGMEDIUM parameter because it is responsible for releasing the medium if it is not TYMED_NULL.

For cache connections (<a href="https://msdn.microsoft.com/2a86063a-3ee6-4fc2-a6e0-6e9ffa658348">IOleCache::Cache</a>), this flag requests that the cache not be updated by changes made to the running object. Instead, the container will update the cache by explicitly calling <a href="https://msdn.microsoft.com/b826411d-6e00-44ba-8603-85db40c4a55f">IOleCache::SetData</a>. This situation typically occurs when the iconic aspect of an object is being cached. 

ADVF_NODATA is not a valid flag for view advisory connections (<a href="https://msdn.microsoft.com/64712679-8454-41fa-9497-f0ab97240a51">IViewObject::SetAdvise</a>) and it returns E_INVALIDARG.


### -field ADVF_PRIMEFIRST

Requests that the object not wait for the data or view to change before making an initial call to <a href="https://msdn.microsoft.com/834a5328-3a1f-4edb-aad0-be8ab87acb04">IAdviseSink::OnDataChange</a> (for data or view advisory connections) or updating the cache (for cache connections). Used with ADVF_ONLYONCE, this parameter provides an asynchronous <a href="https://msdn.microsoft.com/05118461-0438-4715-b2c2-fc2471ce38f0">IDataObject::GetData</a> call.


### -field ADVF_ONLYONCE

Requests that the object make only one change notification or cache update before deleting the connection. 

ADVF_ONLYONCE automatically deletes the advisory connection after sending one data or view notification. The advisory sink receives only one <a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a> call. A nonzero connection identifier is returned if the connection is established, so the caller can use it to delete the connection prior to the first change notification. 

For data change notifications, the combination of ADVF_ONLYONCE and ADVF_PRIMEFIRST provides, in effect, an asynchronous <a href="https://msdn.microsoft.com/05118461-0438-4715-b2c2-fc2471ce38f0">IDataObject::GetData</a> call. 

When used with caching, ADVF_ONLYONCE updates the cache one time only, on receipt of the first <a href="https://msdn.microsoft.com/834a5328-3a1f-4edb-aad0-be8ab87acb04">IAdviseSink::OnDataChange</a> notification. After the update is complete, the advisory connection between the object and the cache is disconnected. The source object for the advisory connection calls the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method.


### -field ADVF_DATAONSTOP

For data advisory connections, assures accessibility to data. This flag indicates that when the data object is closing, it should call , providing data with the call. Typically, this value is used in combination with ADVF_NODATA. Without th<a href="https://msdn.microsoft.com/834a5328-3a1f-4edb-aad0-be8ab87acb04">IAdviseSink::OnDataChange</a> is value, by the time an <b>OnDataChange</b> call without data reaches the sink, the source might have completed its shutdown and the data might not be accessible. Sinks that specify this value should accept data provided in <b>OnDataChange</b> if it is being passed, because they may not get another chance to retrieve it.

For cache connections, this flag indicates that the object should update the cache as part of object closure.

ADVF_DATAONSTOP is not a valid flag for view advisory connections.


### -field ADVFCACHE_NOHANDLER

Synonym for ADVFCACHE_FORCEBUILTIN, which is used more often.


### -field ADVFCACHE_FORCEBUILTIN

This value is used by DLL object applications and object handlers that perform the drawing of their objects. ADVFCACHE_FORCEBUILTIN instructs OLE to cache presentation data to ensure that there is a presentation in the cache. This value is not a valid flag for data or view advisory connections. For cache connections, this flag caches data that requires only code shipped with OLE (or the underlying operating system) to be present in order to produce it with <a href="https://msdn.microsoft.com/05118461-0438-4715-b2c2-fc2471ce38f0">IDataObject::GetData</a> or <a href="https://msdn.microsoft.com/913593ff-07fe-44bd-88dc-8e58da82089b">IViewObject::Draw</a>. By specifying this value, the container can ensure that the data can be retrieved even when the object or handler code is not available. 


### -field ADVFCACHE_ONSAVE

For cache connections, this flag updates the cached representation only when the object containing the cache is saved. The cache is also updated when the OLE object transitions from the running state back to the loaded state (because a subsequent save operation would require rerunning the object). This value is not a valid flag for data or view advisory connections.


## -remarks



For a data or view advisory connection, the container uses the <b>ADVF</b> constants when setting up a connection between an <a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a> instance and either an <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> or <a href="https://msdn.microsoft.com/4310c987-3542-4a59-a6fb-951143001741">IViewObject</a> instance. These connections are set up using the <a href="https://msdn.microsoft.com/be9891d4-aad3-42a0-8c8e-4b86091ff03b">IDataObject::DAdvise</a>, <a href="https://msdn.microsoft.com/3b72a50b-a18f-4ec0-9d1d-52b07eb84faf">IDataAdviseHolder::Advise</a>, or <a href="https://msdn.microsoft.com/64712679-8454-41fa-9497-f0ab97240a51">IViewObject::SetAdvise</a> methods.



For a caching connection, the constants are specified in the <a href="https://msdn.microsoft.com/2a86063a-3ee6-4fc2-a6e0-6e9ffa658348">IOleCache::Cache</a>method to indicate the container's requests on how the object should update its cache.



These constants are also used in the <b>advf</b> member of the <a href="https://msdn.microsoft.com/f31469b2-4a4a-4da5-9229-38ddd0bcc88e">STATDATA</a> structure. This structure is used by <a href="https://msdn.microsoft.com/8e2f6655-4a09-4868-a909-18999104b3ff">IEnumSTATDATA</a> to describe the enumerated connections, and the <b>advf</b> member indicates the flags that were specified when the advisory or cache connection was established. When <b>STATDATA</b> is used for an<a href="https://msdn.microsoft.com/4e1d6d9e-ebf2-4cd6-b7b4-00f9e7bd9bdc"> IOleObject::EnumAdvise</a> enumerator, the <b>advf</b> member is indeterminate.





## -see-also




<a href="https://msdn.microsoft.com/740a6366-6ab1-4a20-82df-1efdd62211eb">IDataAdviseHolder</a>



<a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>



<a href="https://msdn.microsoft.com/8e2f6655-4a09-4868-a909-18999104b3ff">IEnumSTATDATA</a>



<a href="https://msdn.microsoft.com/b5ef85d0-b54e-4831-87f1-ac6763179181">IOleCache</a>



<a href="https://msdn.microsoft.com/4310c987-3542-4a59-a6fb-951143001741">IViewObject</a>
 

 

