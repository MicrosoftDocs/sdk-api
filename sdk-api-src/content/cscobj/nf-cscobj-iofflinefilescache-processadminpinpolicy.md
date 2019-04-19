---
UID: NF:cscobj.IOfflineFilesCache.ProcessAdminPinPolicy
title: IOfflineFilesCache::ProcessAdminPinPolicy (cscobj.h)
author: windows-sdk-content
description: Causes Offline Files to process the &#0034;administratively assigned offline files&#0034; group policy.
old-location: of\iofflinefilescache_processadminpinpolicy.htm
tech.root: offlinefiles
ms.assetid: 25ee4586-3031-4815-9a35-ce57cf9366d7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOfflineFilesCache interface [Offline Files],ProcessAdminPinPolicy method, IOfflineFilesCache.ProcessAdminPinPolicy, IOfflineFilesCache::ProcessAdminPinPolicy, ProcessAdminPinPolicy, ProcessAdminPinPolicy method [Offline Files], ProcessAdminPinPolicy method [Offline Files],IOfflineFilesCache interface, cscobj/IOfflineFilesCache::ProcessAdminPinPolicy, of.iofflinefilescache_processadminpinpolicy
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesCache::ProcessAdminPinPolicy


## -description


Causes Offline Files to process the "administratively assigned offline files" group policy.


## -parameters




### -param pPinProgress [in]

Pointer to the <a href="https://msdn.microsoft.com/7fc5ff29-be9d-4fad-96a8-94058bb708fa">IOfflineFilesSyncProgress</a> interface that receives progress notifications as items are being pinned in the Offline Files cache.


### -param pUnpinProgress [in]

Pointer to the <a href="https://msdn.microsoft.com/7fc5ff29-be9d-4fad-96a8-94058bb708fa">IOfflineFilesSyncProgress</a> interface that receives progress notifications as items are being unpinned from the Offline Files cache.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



The "administratively assigned offline files" group policy provides a way for administrators to cause specific folders to be pinned by Offline Files for specific users by way of the Group Policy mechanism.  The primary client of this function is the Offline Files Group Policy extension.  In most deployments there is no need to call this function.  The Group Policy extension will do that for you.




## -see-also




<a href="https://msdn.microsoft.com/7b1b5ef6-355a-4760-9d54-ec73cc66fb8a">IOfflineFilesCache</a>
 

 

