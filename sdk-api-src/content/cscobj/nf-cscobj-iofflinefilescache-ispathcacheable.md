---
UID: NF:cscobj.IOfflineFilesCache.IsPathCacheable
title: IOfflineFilesCache::IsPathCacheable (cscobj.h)
description: Determines whether a specified UNC path is in the Offline Files cache.
helpviewer_keywords: ["IOfflineFilesCache interface [Offline Files]","IsPathCacheable method","IOfflineFilesCache.IsPathCacheable","IOfflineFilesCache::IsPathCacheable","IsPathCacheable","IsPathCacheable method [Offline Files]","IsPathCacheable method [Offline Files]","IOfflineFilesCache interface","OFFLINEFILES_CACHING_MODE_AUTO_DOC","OFFLINEFILES_CACHING_MODE_AUTO_PROGANDDOC","OFFLINEFILES_CACHING_MODE_MANUAL","OFFLINEFILES_CACHING_MODE_NOCACHING","OFFLINEFILES_CACHING_MODE_NONE","cscobj/IOfflineFilesCache::IsPathCacheable","of.iofflinefilescache_ispathcacheable"]
old-location: of\iofflinefilescache_ispathcacheable.htm
tech.root: of
ms.assetid: 4d9a2fda-baad-4ada-8a07-f39c9cfafdfa
ms.date: 12/05/2018
ms.keywords: IOfflineFilesCache interface [Offline Files],IsPathCacheable method, IOfflineFilesCache.IsPathCacheable, IOfflineFilesCache::IsPathCacheable, IsPathCacheable, IsPathCacheable method [Offline Files], IsPathCacheable method [Offline Files],IOfflineFilesCache interface, OFFLINEFILES_CACHING_MODE_AUTO_DOC, OFFLINEFILES_CACHING_MODE_AUTO_PROGANDDOC, OFFLINEFILES_CACHING_MODE_MANUAL, OFFLINEFILES_CACHING_MODE_NOCACHING, OFFLINEFILES_CACHING_MODE_NONE, cscobj/IOfflineFilesCache::IsPathCacheable, of.iofflinefilescache_ispathcacheable
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOfflineFilesCache::IsPathCacheable
 - cscobj/IOfflineFilesCache::IsPathCacheable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesCache.IsPathCacheable
---

# IOfflineFilesCache::IsPathCacheable


## -description

Determines whether a specified UNC path is in the Offline Files cache.

## -parameters

### -param pszPath [in]

The UNC path of the item.

### -param pbCacheable [out]

Receives <b>TRUE</b> if the item is in the Offline Files cache, <b>FALSE</b> if not.

### -param pShareCachingMode [out]

Receives one of the following <a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_caching_mode">OFFLINEFILES_CACHING_MODE</a> enumeration values indicating the caching configuration of the applicable network shared folder under which the specified item exists.



#### OFFLINEFILES_CACHING_MODE_NONE (0)

No caching mode value was found.  This value is used when the item is not cacheable or an error has occurred.



#### OFFLINEFILES_CACHING_MODE_NOCACHING (1)

The shared folder is configured to disallow caching.



#### OFFLINEFILES_CACHING_MODE_MANUAL (2)

The shared folder is configured to allow manual caching.



#### OFFLINEFILES_CACHING_MODE_AUTO_DOC (3)

The shared folder is configured to allow automatic caching of documents.



#### OFFLINEFILES_CACHING_MODE_AUTO_PROGANDDOC (4)

The shared folder is configured to allow automatic caching of programs and documents.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

The caching mode value returned is equivalent to the <b>CSC_MASK</b> value associated with <a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1005">SHARE_INFO_1005</a> returned by <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo">NetShareGetInfo</a>.  The value mapping is as follows:

<table>
<tr>
<th>
<a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_caching_mode">OFFLINEFILES_CACHING_MODE</a> Value</th>
<th>
<a href="/windows/desktop/api/lmshare/ns-lmshare-share_info_1005">SHARE_INFO_1005</a> Value</th>
</tr>
<tr>
<td><b>OFFLINEFILES_CACHING_MODE_NOCACHING</b></td>
<td>0</td>
</tr>
<tr>
<td><b>OFFLINEFILES_CACHING_MODE_MANUAL</b></td>
<td><b>CSC_CACHE_MANUAL_REINT</b></td>
</tr>
<tr>
<td><b>OFFLINEFILES_CACHING_MODE_AUTO_DOC</b></td>
<td><b>CSC_CACHE_AUTO_REINT</b></td>
</tr>
<tr>
<td><b>OFFLINEFILES_CACHING_MODE_AUTO_PROGANDDOC</b></td>
<td><b>CSC_CACHE_VDO</b></td>
</tr>
</table>
 

These settings are configured as attributes of the shared folder on the server by clicking the Caching button on the shared folder's Sharing property page or by using the <code>net share /cache</code> command.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilescache">IOfflineFilesCache</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesshareinfo-getsharecachingmode">IOfflineFilesShareInfo::GetShareCachingMode</a>



<a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_caching_mode">OFFLINEFILES_CACHING_MODE</a>