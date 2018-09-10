---
UID: NF:oleidl.IOleCache2.UpdateCache
title: IOleCache2::UpdateCache
author: windows-sdk-content
description: Updates the specified caches. This method is used when the application needs precise control over caching.
old-location: com\iolecache2_updatecache.htm
tech.root: com
ms.assetid: 67bb0bcf-981a-4b2f-8ab9-2afc0659b2db
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IOleCache2 interface [COM],UpdateCache method, IOleCache2.UpdateCache, IOleCache2::UpdateCache, UPDFCACHE_ ALLBUTNODATACACHE, UPDFCACHE_ IFBLANKORONSAVECACHE, UPDFCACHE_ALL, UPDFCACHE_IFBLANK, UPDFCACHE_NODATACACHE, UPDFCACHE_NORMALCACHE, UPDFCACHE_ONLYIFBLANK, UPDFCACHE_ONSAVECACHE, UPDFCACHE_ONSTOPCACHE, UpdateCache, UpdateCache method [COM], UpdateCache method [COM],IOleCache2 interface, _ole_iolecache2_updatecache, com.iolecache2_updatecache, oleidl/IOleCache2::UpdateCache
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IOleCache2.UpdateCache
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleCache2::UpdateCache


## -description


Updates the specified caches. This method is used when the application needs precise control over caching.


## -parameters




### -param pDataObject [in]

A pointer to the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface on the data object from which the cache is updated. Object handlers and in-process servers typically pass a non-<b>NULL</b> value. A container application usually passes <b>NULL</b>, and the source is obtained from the currently running object.


### -param grfUpdf [in]

The type of cache to be updated. This parameter can be one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="UPDFCACHE_NODATACACHE_"></a><a id="updfcache_nodatacache_"></a><dl>
<dt><b>UPDFCACHE_NODATACACHE
</b></dt>
</dl>
</td>
<td width="60%">
Updates caches created by using ADVF_NODATA in the call to <a href="https://msdn.microsoft.com/2a86063a-3ee6-4fc2-a6e0-6e9ffa658348">IOleCache::Cache</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="UPDFCACHE_ONSAVECACHE_"></a><a id="updfcache_onsavecache_"></a><dl>
<dt><b>UPDFCACHE_ONSAVECACHE
</b></dt>
</dl>
</td>
<td width="60%">
Updates caches created by using ADVFCACHE_ONSAVE in the call to <a href="https://msdn.microsoft.com/2a86063a-3ee6-4fc2-a6e0-6e9ffa658348">IOleCache::Cache</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="UPDFCACHE_ONSTOPCACHE_"></a><a id="updfcache_onstopcache_"></a><dl>
<dt><b>UPDFCACHE_ONSTOPCACHE
</b></dt>
</dl>
</td>
<td width="60%">
Updates caches created by using ADVFCACHE_ONSTOP in the call to <a href="https://msdn.microsoft.com/2a86063a-3ee6-4fc2-a6e0-6e9ffa658348">IOleCache::Cache</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="UPDFCACHE_NORMALCACHE"></a><a id="updfcache_normalcache"></a><dl>
<dt><b>UPDFCACHE_NORMALCACHE</b></dt>
</dl>
</td>
<td width="60%">
Dynamically updates the caches (as is normally done when the object sends out <a href="https://msdn.microsoft.com/834a5328-3a1f-4edb-aad0-be8ab87acb04">OnDataChange</a> notices).

</td>
</tr>
<tr>
<td width="40%"><a id="UPDFCACHE_IFBLANK"></a><a id="updfcache_ifblank"></a><dl>
<dt><b>UPDFCACHE_IFBLANK</b></dt>
</dl>
</td>
<td width="60%">
Updates the cache if blank, regardless of any other flag specified.

</td>
</tr>
<tr>
<td width="40%"><a id="UPDFCACHE_ONLYIFBLANK"></a><a id="updfcache_onlyifblank"></a><dl>
<dt><b>UPDFCACHE_ONLYIFBLANK</b></dt>
</dl>
</td>
<td width="60%">
Updates only caches that are blank.

</td>
</tr>
<tr>
<td width="40%"><a id="UPDFCACHE__IFBLANKORONSAVECACHE"></a><a id="updfcache__ifblankoronsavecache"></a><dl>
<dt><b>UPDFCACHE_ IFBLANKORONSAVECACHE</b></dt>
</dl>
</td>
<td width="60%">
The equivalent of using an OR operation to combine UPDFCACHE_IFBLANK and UPDFCACHE_ONSAVECACHE.

</td>
</tr>
<tr>
<td width="40%"><a id="UPDFCACHE_ALL"></a><a id="updfcache_all"></a><dl>
<dt><b>UPDFCACHE_ALL</b></dt>
</dl>
</td>
<td width="60%">
Updates all caches.

</td>
</tr>
<tr>
<td width="40%"><a id="UPDFCACHE__ALLBUTNODATACACHE"></a><a id="updfcache__allbutnodatacache"></a><dl>
<dt><b>UPDFCACHE_ ALLBUTNODATACACHE</b></dt>
</dl>
</td>
<td width="60%">
Updates all caches except those created with ADVF_NODATA in the call to <a href="https://msdn.microsoft.com/2a86063a-3ee6-4fc2-a6e0-6e9ffa658348">IOleCache::Cache</a>. Thus, you can control updates to the caches created with the ADVF_NODATA flag and only update these caches explicitly.


</td>
</tr>
</table>
 


### -param pReserved [in]

This parameter is reserved and must be <b>NULL</b>.


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
One of the arguments is not valid.

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
Insufficient memory is available for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_NOTRUNNING</b></dt>
</dl>
</td>
<td width="60%">
The specified <i>pDataObject</i> is not running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CACHE_E_NOCACHE_UPDATED</b></dt>
</dl>
</td>
<td width="60%">
None of the caches were updated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CACHE_S_SOMECACHES_NOTUPDATED</b></dt>
</dl>
</td>
<td width="60%">
Some of the caches were updated.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a>



<a href="https://msdn.microsoft.com/b5ef85d0-b54e-4831-87f1-ac6763179181">IOleCache</a>



<a href="https://msdn.microsoft.com/8bbeca2d-c805-4116-b918-e2ddded8b160">IOleCache2</a>



<a href="https://msdn.microsoft.com/64cc7a29-0bbb-4535-a7b5-9b1d82ad7e8a">IOleCacheControl</a>
 

 

