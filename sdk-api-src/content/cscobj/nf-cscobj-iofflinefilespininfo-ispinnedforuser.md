---
UID: NF:cscobj.IOfflineFilesPinInfo.IsPinnedForUser
title: IOfflineFilesPinInfo::IsPinnedForUser (cscobj.h)
description: Determines whether the item was pinned by a user.
helpviewer_keywords: ["IOfflineFilesPinInfo interface [Offline Files]","IsPinnedForUser method","IOfflineFilesPinInfo.IsPinnedForUser","IOfflineFilesPinInfo::IsPinnedForUser","IsPinnedForUser","IsPinnedForUser method [Offline Files]","IsPinnedForUser method [Offline Files]","IOfflineFilesPinInfo interface","cscobj/IOfflineFilesPinInfo::IsPinnedForUser","of.iofflinefilespininfo_ispinnedforuser"]
old-location: of\iofflinefilespininfo_ispinnedforuser.htm
tech.root: of
ms.assetid: d0064423-b173-40e5-96c6-dd6dcf05598d
ms.date: 12/05/2018
ms.keywords: IOfflineFilesPinInfo interface [Offline Files],IsPinnedForUser method, IOfflineFilesPinInfo.IsPinnedForUser, IOfflineFilesPinInfo::IsPinnedForUser, IsPinnedForUser, IsPinnedForUser method [Offline Files], IsPinnedForUser method [Offline Files],IOfflineFilesPinInfo interface, cscobj/IOfflineFilesPinInfo::IsPinnedForUser, of.iofflinefilespininfo_ispinnedforuser
f1_keywords:
- cscobj/IOfflineFilesPinInfo.IsPinnedForUser
dev_langs:
- c++
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
- IOfflineFilesPinInfo.IsPinnedForUser
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesPinInfo::IsPinnedForUser


## -description


Determines whether the item was pinned by a user.


## -parameters




### -param pbPinnedForUser [out]

Receives  <b>TRUE</b> if the item was pinned by a user, or <b>FALSE</b> otherwise.


### -param pbInherit [out]

Receives <b>TRUE</b> if the pinned state is inherited by new child items, or <b>FALSE</b> otherwise.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



When an item is pinned in the Offline Files cache, it is protected from automatic eviction and is guaranteed to be available offline.

This method corresponds to the OFFLINEFILES_PIN_CONTROL_FLAG_FORUSER pin control flag used by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-pin">IOfflineFilesCache::Pin</a> method.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-pin">IOfflineFilesCache::Pin</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilespininfo">IOfflineFilesPinInfo</a>
 

 

