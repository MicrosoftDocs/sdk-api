---
UID: NF:cscobj.IOfflineFilesEvents.ItemAvailableOffline
title: IOfflineFilesEvents::ItemAvailableOffline (cscobj.h)
description: Reports that an item in the Offline Files cache is now available for offline use should the remote copy become unavailable.
helpviewer_keywords: ["IOfflineFilesEvents interface [Offline Files]","ItemAvailableOffline method","IOfflineFilesEvents.ItemAvailableOffline","IOfflineFilesEvents::ItemAvailableOffline","ItemAvailableOffline","ItemAvailableOffline method [Offline Files]","ItemAvailableOffline method [Offline Files]","IOfflineFilesEvents interface","cscobj/IOfflineFilesEvents::ItemAvailableOffline","of.iofflinefilesevents_itemavailableoffline"]
old-location: of\iofflinefilesevents_itemavailableoffline.htm
tech.root: of
ms.assetid: 6c629ede-00ee-4f5e-9f75-022e3c5b3957
ms.date: 12/05/2018
ms.keywords: IOfflineFilesEvents interface [Offline Files],ItemAvailableOffline method, IOfflineFilesEvents.ItemAvailableOffline, IOfflineFilesEvents::ItemAvailableOffline, ItemAvailableOffline, ItemAvailableOffline method [Offline Files], ItemAvailableOffline method [Offline Files],IOfflineFilesEvents interface, cscobj/IOfflineFilesEvents::ItemAvailableOffline, of.iofflinefilesevents_itemavailableoffline
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
 - IOfflineFilesEvents::ItemAvailableOffline
 - cscobj/IOfflineFilesEvents::ItemAvailableOffline
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
 - IOfflineFilesEvents.ItemAvailableOffline
---

# IOfflineFilesEvents::ItemAvailableOffline


## -description

Reports that an item in the Offline Files cache is now available for offline use should the remote copy become unavailable.

## -parameters

### -param pszPath [in]

The item's UNC path string.

### -param ItemType [in]

An <a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_item_type">OFFLINEFILES_ITEM_TYPE</a> enumeration value that indicates the type of the item.

## -returns

The return value is ignored.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesevents">IOfflineFilesEvents</a>