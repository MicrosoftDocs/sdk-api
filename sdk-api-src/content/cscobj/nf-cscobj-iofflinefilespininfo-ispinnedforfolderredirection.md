---
UID: NF:cscobj.IOfflineFilesPinInfo.IsPinnedForFolderRedirection
title: IOfflineFilesPinInfo::IsPinnedForFolderRedirection (cscobj.h)
description: Determines whether the item was pinned by Folder Redirection.
helpviewer_keywords: ["IOfflineFilesPinInfo interface [Offline Files]","IsPinnedForFolderRedirection method","IOfflineFilesPinInfo.IsPinnedForFolderRedirection","IOfflineFilesPinInfo::IsPinnedForFolderRedirection","IsPinnedForFolderRedirection","IsPinnedForFolderRedirection method [Offline Files]","IsPinnedForFolderRedirection method [Offline Files]","IOfflineFilesPinInfo interface","cscobj/IOfflineFilesPinInfo::IsPinnedForFolderRedirection","of.iofflinefilespininfo_ispinnedforfolderredirection"]
old-location: of\iofflinefilespininfo_ispinnedforfolderredirection.htm
tech.root: of
ms.assetid: b832f75a-3cd4-4421-a0a5-22c5682cb4c3
ms.date: 12/05/2018
ms.keywords: IOfflineFilesPinInfo interface [Offline Files],IsPinnedForFolderRedirection method, IOfflineFilesPinInfo.IsPinnedForFolderRedirection, IOfflineFilesPinInfo::IsPinnedForFolderRedirection, IsPinnedForFolderRedirection, IsPinnedForFolderRedirection method [Offline Files], IsPinnedForFolderRedirection method [Offline Files],IOfflineFilesPinInfo interface, cscobj/IOfflineFilesPinInfo::IsPinnedForFolderRedirection, of.iofflinefilespininfo_ispinnedforfolderredirection
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
 - IOfflineFilesPinInfo::IsPinnedForFolderRedirection
 - cscobj/IOfflineFilesPinInfo::IsPinnedForFolderRedirection
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
 - IOfflineFilesPinInfo.IsPinnedForFolderRedirection
---

# IOfflineFilesPinInfo::IsPinnedForFolderRedirection


## -description

Determines whether the item was pinned by Folder Redirection.

## -parameters

### -param pbPinnedForFolderRedirection [out]

Receives  <b>TRUE</b> if the item was pinned for users by Folder Redirection, or <b>FALSE</b> otherwise.

### -param pbInherit [out]

Receives <b>TRUE</b> if the pinned state is inherited by new child items, or <b>FALSE</b> otherwise.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

When an item is pinned in the Offline Files cache, it is protected from automatic eviction and is guaranteed to be available offline.

This method corresponds to the OFFLINEFILES_PIN_CONTROL_FLAG_FORREDIR pin control flag used by the <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-pin">IOfflineFilesCache::Pin</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-pin">IOfflineFilesCache::Pin</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilespininfo">IOfflineFilesPinInfo</a>