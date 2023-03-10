---
UID: NF:cscobj.IOfflineFilesCache.ProcessAdminPinPolicy
title: IOfflineFilesCache::ProcessAdminPinPolicy (cscobj.h)
description: Causes Offline Files to process the &quot;administratively assigned offline files&quot; group policy.
helpviewer_keywords: ["IOfflineFilesCache interface [Offline Files]","ProcessAdminPinPolicy method","IOfflineFilesCache.ProcessAdminPinPolicy","IOfflineFilesCache::ProcessAdminPinPolicy","ProcessAdminPinPolicy","ProcessAdminPinPolicy method [Offline Files]","ProcessAdminPinPolicy method [Offline Files]","IOfflineFilesCache interface","cscobj/IOfflineFilesCache::ProcessAdminPinPolicy","of.iofflinefilescache_processadminpinpolicy"]
old-location: of\iofflinefilescache_processadminpinpolicy.htm
tech.root: of
ms.assetid: 25ee4586-3031-4815-9a35-ce57cf9366d7
ms.date: 12/05/2018
ms.keywords: IOfflineFilesCache interface [Offline Files],ProcessAdminPinPolicy method, IOfflineFilesCache.ProcessAdminPinPolicy, IOfflineFilesCache::ProcessAdminPinPolicy, ProcessAdminPinPolicy, ProcessAdminPinPolicy method [Offline Files], ProcessAdminPinPolicy method [Offline Files],IOfflineFilesCache interface, cscobj/IOfflineFilesCache::ProcessAdminPinPolicy, of.iofflinefilescache_processadminpinpolicy
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
 - IOfflineFilesCache::ProcessAdminPinPolicy
 - cscobj/IOfflineFilesCache::ProcessAdminPinPolicy
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
 - IOfflineFilesCache.ProcessAdminPinPolicy
---

# IOfflineFilesCache::ProcessAdminPinPolicy


## -description

Causes Offline Files to process the "administratively assigned offline files" group policy.

## -parameters

### -param pPinProgress [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncprogress">IOfflineFilesSyncProgress</a> interface that receives progress notifications as items are being pinned in the Offline Files cache.

### -param pUnpinProgress [in]

Pointer to the <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncprogress">IOfflineFilesSyncProgress</a> interface that receives progress notifications as items are being unpinned from the Offline Files cache.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

The "administratively assigned offline files" group policy provides a way for administrators to cause specific folders to be pinned by Offline Files for specific users by way of the Group Policy mechanism.  The primary client of this function is the Offline Files Group Policy extension.  In most deployments there is no need to call this function.  The Group Policy extension will do that for you.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilescache">IOfflineFilesCache</a>