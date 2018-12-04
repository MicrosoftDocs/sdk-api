---
UID: NF:oleidl.IOleCache.InitCache
title: IOleCache::InitCache
author: windows-sdk-content
description: Fills the cache as needed using the data provided by the specified data object.
old-location: com\iolecache_initcache.htm
tech.root: com
ms.assetid: 4b1f2fb6-636c-47dd-8f89-884f7b4f3977
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IOleCache interface [COM],InitCache method, IOleCache.InitCache, IOleCache::InitCache, InitCache, InitCache method [COM], InitCache method [COM],IOleCache interface, _ole_iolecache_initcache, com.iolecache_initcache, oleidl/IOleCache::InitCache
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
 - IOleCache.InitCache
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleCache::InitCache


## -description


Fills the cache as needed using the data provided by the specified data object.


## -parameters




### -param pDataObject [in]

A pointer to the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface on the data object from which the cache is to be initialized.


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
The pointer to the <a href="https://msdn.microsoft.com/8a002deb-2727-456c-8078-a9b0d5893ed4">IDataObject</a> interface is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory is available for the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_NOTRUNNING</b></dt>
</dl>
</td>
<td width="60%">
The cache is not running.

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
Only some of the existing caches were updated.

</td>
</tr>
</table>
 




## -remarks



<b>InitCache</b> is usually used when creating an object from a drag-and-drop operation or from a clipboard paste operation. It fills the cache as needed with presentation data from all the data formats provided by the data object provided on the clipboard or in the drag-and-drop operation. Helper functions like <a href="https://msdn.microsoft.com/aa5e997e-60d4-472d-9c81-5359c277bde3">OleCreateFromData</a> or <a href="https://msdn.microsoft.com/3eda0cf5-c33d-43cf-ba8a-02a4f6383adc">OleCreateLinkFromData</a> call this method when needed. If a container does not use these helper functions to create compound document objects, it can use <a href="https://msdn.microsoft.com/2a86063a-3ee6-4fc2-a6e0-6e9ffa658348">IOleCache::Cache</a> to set up the cache entries which are then filled by <b>InitCache</b>.





## -see-also




<a href="https://msdn.microsoft.com/b5ef85d0-b54e-4831-87f1-ac6763179181">IOleCache</a>



<a href="https://msdn.microsoft.com/2a86063a-3ee6-4fc2-a6e0-6e9ffa658348">IOleCache::Cache</a>
 

 

