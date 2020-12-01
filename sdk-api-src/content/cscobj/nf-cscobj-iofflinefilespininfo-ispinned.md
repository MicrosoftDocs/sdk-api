---
UID: NF:cscobj.IOfflineFilesPinInfo.IsPinned
title: IOfflineFilesPinInfo::IsPinned (cscobj.h)
description: Determines whether the item is pinned.
helpviewer_keywords: ["IOfflineFilesPinInfo interface [Offline Files]","IsPinned method","IOfflineFilesPinInfo.IsPinned","IOfflineFilesPinInfo::IsPinned","IsPinned","IsPinned method [Offline Files]","IsPinned method [Offline Files]","IOfflineFilesPinInfo interface","cscobj/IOfflineFilesPinInfo::IsPinned","of.iofflinefilespininfo_ispinned"]
old-location: of\iofflinefilespininfo_ispinned.htm
tech.root: of
ms.assetid: 143cf346-dbe0-42cf-871e-a0cb54722403
ms.date: 12/05/2018
ms.keywords: IOfflineFilesPinInfo interface [Offline Files],IsPinned method, IOfflineFilesPinInfo.IsPinned, IOfflineFilesPinInfo::IsPinned, IsPinned, IsPinned method [Offline Files], IsPinned method [Offline Files],IOfflineFilesPinInfo interface, cscobj/IOfflineFilesPinInfo::IsPinned, of.iofflinefilespininfo_ispinned
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
 - IOfflineFilesPinInfo::IsPinned
 - cscobj/IOfflineFilesPinInfo::IsPinned
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
 - IOfflineFilesPinInfo.IsPinned
---

# IOfflineFilesPinInfo::IsPinned


## -description

Determines whether the item is pinned.

## -parameters

### -param pbPinned [out]

Receives <b>TRUE</b> if the item is pinned for any reason, or <b>FALSE</b> otherwise.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

When an item is pinned in the Offline Files cache, it is protected from automatic eviction and is guaranteed to be available offline.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-pin">IOfflineFilesCache::Pin</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilespininfo">IOfflineFilesPinInfo</a>