---
UID: NF:cscobj.IOfflineFilesCache.RenameItem
title: IOfflineFilesCache::RenameItem (cscobj.h)
description: Renames an item in the cache.
helpviewer_keywords: ["IOfflineFilesCache interface [Offline Files]","RenameItem method","IOfflineFilesCache.RenameItem","IOfflineFilesCache::RenameItem","RenameItem","RenameItem method [Offline Files]","RenameItem method [Offline Files]","IOfflineFilesCache interface","cscobj/IOfflineFilesCache::RenameItem","of.iofflinefilescache_renameitem"]
old-location: of\iofflinefilescache_renameitem.htm
tech.root: of
ms.assetid: 883f29cb-d551-4358-8e74-f901956d8829
ms.date: 12/05/2018
ms.keywords: IOfflineFilesCache interface [Offline Files],RenameItem method, IOfflineFilesCache.RenameItem, IOfflineFilesCache::RenameItem, RenameItem, RenameItem method [Offline Files], RenameItem method [Offline Files],IOfflineFilesCache interface, cscobj/IOfflineFilesCache::RenameItem, of.iofflinefilescache_renameitem
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
 - IOfflineFilesCache::RenameItem
 - cscobj/IOfflineFilesCache::RenameItem
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
 - IOfflineFilesCache.RenameItem
---

# IOfflineFilesCache::RenameItem


## -description

Renames an item in the cache. This method logs a request with the Offline Files service for a path to be renamed on the next system restart.

## -parameters

### -param pszPathOriginal [in]

Fully qualified UNC path of the item (server, share, file or directory) to be renamed.

### -param pszPathNew [in]

The new path to replace <i>pszPathOriginal</i> if the item that  <i>pszPathOriginal</i> points to exists in the cache.

### -param bReplaceIfExists [in]

This parameter is reserved for future use.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

This method requires system administrator privilege.

<div class="alert"><b>Note</b>  A restart of the system is necessary for the rename operation to be applied to the Offline Files cache.</div>
<div> </div>
This method fails if the path referenced by the <i>pszPathNew</i> parameter already exists in the Offline Files cache.

Beginning with Windows 8 and Windows Server 2012 you can also use the <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache2-renameitemex">IOfflineFilesCache2::RenameItemEx</a> method to rename an item. It does not require system administrator privilege or a system restart. However, it will fail if the item is currently in use.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilescache">IOfflineFilesCache</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache2-renameitemex">IOfflineFilesCache2::RenameItemEx</a>