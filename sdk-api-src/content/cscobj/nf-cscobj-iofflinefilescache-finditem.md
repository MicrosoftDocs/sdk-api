---
UID: NF:cscobj.IOfflineFilesCache.FindItem
title: IOfflineFilesCache::FindItem (cscobj.h)
description: Locates a particular file or directory item in the cache.
helpviewer_keywords: ["FindItem","FindItem method [Offline Files]","FindItem method [Offline Files]","IOfflineFilesCache interface","IOfflineFilesCache interface [Offline Files]","FindItem method","IOfflineFilesCache.FindItem","IOfflineFilesCache::FindItem","OFFLINEFILES_ITEM_QUERY_ADMIN","OFFLINEFILES_ITEM_QUERY_CONNECTIONSTATE","OFFLINEFILES_ITEM_QUERY_INCLUDETRANSPARENTCACHE","OFFLINEFILES_ITEM_QUERY_LOCALDIRTYBYTECOUNT","OFFLINEFILES_ITEM_QUERY_REMOTEDIRTYBYTECOUNT","OFFLINEFILES_ITEM_QUERY_REMOTEINFO","cscobj/IOfflineFilesCache::FindItem","of.iofflinefilescache_finditem"]
old-location: of\iofflinefilescache_finditem.htm
tech.root: of
ms.assetid: 15696dbf-09a9-42e3-8400-20f7b9b171b7
ms.date: 12/05/2018
ms.keywords: FindItem, FindItem method [Offline Files], FindItem method [Offline Files],IOfflineFilesCache interface, IOfflineFilesCache interface [Offline Files],FindItem method, IOfflineFilesCache.FindItem, IOfflineFilesCache::FindItem, OFFLINEFILES_ITEM_QUERY_ADMIN, OFFLINEFILES_ITEM_QUERY_CONNECTIONSTATE, OFFLINEFILES_ITEM_QUERY_INCLUDETRANSPARENTCACHE, OFFLINEFILES_ITEM_QUERY_LOCALDIRTYBYTECOUNT, OFFLINEFILES_ITEM_QUERY_REMOTEDIRTYBYTECOUNT, OFFLINEFILES_ITEM_QUERY_REMOTEINFO, cscobj/IOfflineFilesCache::FindItem, of.iofflinefilescache_finditem
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
 - IOfflineFilesCache::FindItem
 - cscobj/IOfflineFilesCache::FindItem
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
 - IOfflineFilesCache.FindItem
---

# IOfflineFilesCache::FindItem


## -description

Locates a particular file or directory item in the cache.

## -parameters

### -param pszPath [in]

UNC path of the file or directory to be located.

### -param dwQueryFlags [in]

Flags affecting the amount of query activity at the time the item is located in the cache. The parameter may contain one or more of the following bit flags.



#### OFFLINEFILES_ITEM_QUERY_REMOTEINFO (0x00000001)

This flag is reserved for future use.



#### OFFLINEFILES_ITEM_QUERY_CONNECTIONSTATE (0x00000002)

If this flag is set, the find operation includes an extra call to the Offline Files store to obtain information about the connection state (online/offline) of the item. If this flag is not set, the operation does not include this extra operation, and connection state will be queried on demand when it is requested.

<div class="alert"><b>Note</b>  If you know that you will need the connection state for the item, setting this flag is slightly more efficient.  If the connection state is not required, it is more efficient to not set this flag.</div>
<div> </div>


#### OFFLINEFILES_ITEM_QUERY_LOCALDIRTYBYTECOUNT (0x00000004)

If this flag is set, the find operation includes an extra call to the Offline Files store to obtain information about the amount, in bytes, of unsynchronized ("dirty") data for the associated file in the local Offline Files cache.



#### OFFLINEFILES_ITEM_QUERY_REMOTEDIRTYBYTECOUNT (0x00000008)

This flag is reserved for future use.



#### OFFLINEFILES_ITEM_QUERY_INCLUDETRANSPARENTCACHE (0x00000010)

If this flag is set, the find operation includes transparently cached items.



#### OFFLINEFILES_ITEM_QUERY_ADMIN (0x80000000)

Allows administrators to find items cached by any user.  If this flag is set and the caller is not an administrator, the method call fails.

### -param ppItem [out]

Pointer to the <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitem">IOfflineFilesItem</a> interface of the cache item.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

Returns <code>HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND)</code> if the cache entry is not found.

## -remarks

<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-finditemex">FindItemEx</a> is an enhanced version of <b>FindItem</b> that provides filtering capabilities similar to what is offered by cache item enumeration.  Calling <b>FindItem</b> is equivalent to calling <b>FindItemEx</b> with all four filter parameters set to <b>NULL</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilescache">IOfflineFilesCache</a>