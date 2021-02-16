---
UID: NF:cscobj.IOfflineFilesPinInfo.IsPinnedForComputer
title: IOfflineFilesPinInfo::IsPinnedForComputer (cscobj.h)
description: Determines whether the item was pinned for all users on the computer by Group Policy.
helpviewer_keywords: ["IOfflineFilesPinInfo interface [Offline Files]","IsPinnedForComputer method","IOfflineFilesPinInfo.IsPinnedForComputer","IOfflineFilesPinInfo::IsPinnedForComputer","IsPinnedForComputer","IsPinnedForComputer method [Offline Files]","IsPinnedForComputer method [Offline Files]","IOfflineFilesPinInfo interface","cscobj/IOfflineFilesPinInfo::IsPinnedForComputer","of.iofflinefilespininfo_ispinnedforcomputer"]
old-location: of\iofflinefilespininfo_ispinnedforcomputer.htm
tech.root: of
ms.assetid: 67d2c444-2498-4848-a4fb-8cae5ff77eaf
ms.date: 12/05/2018
ms.keywords: IOfflineFilesPinInfo interface [Offline Files],IsPinnedForComputer method, IOfflineFilesPinInfo.IsPinnedForComputer, IOfflineFilesPinInfo::IsPinnedForComputer, IsPinnedForComputer, IsPinnedForComputer method [Offline Files], IsPinnedForComputer method [Offline Files],IOfflineFilesPinInfo interface, cscobj/IOfflineFilesPinInfo::IsPinnedForComputer, of.iofflinefilespininfo_ispinnedforcomputer
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
 - IOfflineFilesPinInfo::IsPinnedForComputer
 - cscobj/IOfflineFilesPinInfo::IsPinnedForComputer
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
 - IOfflineFilesPinInfo.IsPinnedForComputer
---

# IOfflineFilesPinInfo::IsPinnedForComputer


## -description

Determines whether the item was pinned for all users on the computer by Group Policy.

## -parameters

### -param pbPinnedForComputer [out]

Receives  <b>TRUE</b> if the item was pinned for users by Group Policy, or <b>FALSE</b> otherwise.

### -param pbInherit [out]

Receives <b>TRUE</b> if the pinned state is inherited by new child items, or <b>FALSE</b> otherwise.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

When an item is pinned in the Offline Files cache, it is protected from automatic eviction and is guaranteed to be available offline.

This method corresponds to the OFFLINEFILES_PIN_CONTROL_FLAG_FORALL pin control flag used by the <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-pin">IOfflineFilesCache::Pin</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-pin">IOfflineFilesCache::Pin</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilespininfo">IOfflineFilesPinInfo</a>