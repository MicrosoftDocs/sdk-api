---
UID: NF:cscobj.IOfflineFilesPinInfo.IsPinnedForUserByPolicy
title: IOfflineFilesPinInfo::IsPinnedForUserByPolicy (cscobj.h)
description: Determines whether the item was pinned for users by Group Policy.
helpviewer_keywords: ["IOfflineFilesPinInfo interface [Offline Files]","IsPinnedForUserByPolicy method","IOfflineFilesPinInfo.IsPinnedForUserByPolicy","IOfflineFilesPinInfo::IsPinnedForUserByPolicy","IsPinnedForUserByPolicy","IsPinnedForUserByPolicy method [Offline Files]","IsPinnedForUserByPolicy method [Offline Files]","IOfflineFilesPinInfo interface","cscobj/IOfflineFilesPinInfo::IsPinnedForUserByPolicy","of.iofflinefilespininfo_ispinnedforuserbypolicy"]
old-location: of\iofflinefilespininfo_ispinnedforuserbypolicy.htm
tech.root: of
ms.assetid: fa5548e9-0a4e-4e66-a5ea-45d092c239b2
ms.date: 12/05/2018
ms.keywords: IOfflineFilesPinInfo interface [Offline Files],IsPinnedForUserByPolicy method, IOfflineFilesPinInfo.IsPinnedForUserByPolicy, IOfflineFilesPinInfo::IsPinnedForUserByPolicy, IsPinnedForUserByPolicy, IsPinnedForUserByPolicy method [Offline Files], IsPinnedForUserByPolicy method [Offline Files],IOfflineFilesPinInfo interface, cscobj/IOfflineFilesPinInfo::IsPinnedForUserByPolicy, of.iofflinefilespininfo_ispinnedforuserbypolicy
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
 - IOfflineFilesPinInfo::IsPinnedForUserByPolicy
 - cscobj/IOfflineFilesPinInfo::IsPinnedForUserByPolicy
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
 - IOfflineFilesPinInfo.IsPinnedForUserByPolicy
---

# IOfflineFilesPinInfo::IsPinnedForUserByPolicy


## -description

Determines whether the item was pinned for users by Group Policy.

## -parameters

### -param pbPinnedForUser [out]

Receives  <b>TRUE</b> if the item was pinned for users by Group Policy, or <b>FALSE</b> otherwise.

### -param pbInherit [out]

Receives <b>TRUE</b> if the pinned state is inherited by new child items, or <b>FALSE</b> otherwise.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

When an item is pinned in the Offline Files cache, it is protected from automatic eviction and is guaranteed to be available offline.

This method corresponds to the OFFLINEFILES_PIN_CONTROL_FLAG_FORUSER_POLICY pin control flag used by the <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-pin">IOfflineFilesCache::Pin</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-pin">IOfflineFilesCache::Pin</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilespininfo">IOfflineFilesPinInfo</a>