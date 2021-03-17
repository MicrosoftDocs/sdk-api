---
UID: NF:cscobj.IOfflineFilesPinInfo2.IsPartlyPinned
title: IOfflineFilesPinInfo2::IsPartlyPinned (cscobj.h)
description: Determines whether the item is partly pinned.
helpviewer_keywords: ["IOfflineFilesPinInfo2 interface [Offline Files]","IsPartlyPinned method","IOfflineFilesPinInfo2.IsPartlyPinned","IOfflineFilesPinInfo2::IsPartlyPinned","IsPartlyPinned","IsPartlyPinned method [Offline Files]","IsPartlyPinned method [Offline Files]","IOfflineFilesPinInfo2 interface","cscobj/IOfflineFilesPinInfo2::IsPartlyPinned","of.iofflinefilespininfo2_ispartlypinned"]
old-location: of\iofflinefilespininfo2_ispartlypinned.htm
tech.root: of
ms.assetid: 9063a804-2597-4959-8249-e5b42f582ea3
ms.date: 12/05/2018
ms.keywords: IOfflineFilesPinInfo2 interface [Offline Files],IsPartlyPinned method, IOfflineFilesPinInfo2.IsPartlyPinned, IOfflineFilesPinInfo2::IsPartlyPinned, IsPartlyPinned, IsPartlyPinned method [Offline Files], IsPartlyPinned method [Offline Files],IOfflineFilesPinInfo2 interface, cscobj/IOfflineFilesPinInfo2::IsPartlyPinned, of.iofflinefilespininfo2_ispartlypinned
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
 - IOfflineFilesPinInfo2::IsPartlyPinned
 - cscobj/IOfflineFilesPinInfo2::IsPartlyPinned
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
 - IOfflineFilesPinInfo2.IsPartlyPinned
---

# IOfflineFilesPinInfo2::IsPartlyPinned


## -description

Determines whether the item is partly pinned.

## -parameters

### -param pbPartlyPinned [out]

Receives <b>TRUE</b> if the item has some child content that is pinned in the Offline Files cache, or <b>FALSE</b> otherwise.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

Only container items, such as directories and shares, can be partly pinned. An item is partly pinned if the item itself is not pinned, but it contains pinned items. The item could contain autocached or transparently cached items in addition to the pinned items.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-pin">IOfflineFilesCache::Pin</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesghostinfo-isghosted">IOfflineFilesGhostInfo::IsGhosted</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilespininfo2">IOfflineFilesPinInfo2</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilestransparentcacheinfo-istransparentlycached">IOfflineFilesTransparentCacheInfo::IsTransparentlyCached</a>