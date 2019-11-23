---
UID: NF:cscobj.IOfflineFilesEvents3.TransparentCacheItemNotify
title: IOfflineFilesEvents3::TransparentCacheItemNotify (cscobj.h)

description: Reports that an action has been performed on a transparently cached item.
old-location: of\iofflinefilesevents3_transparentcacheitemnotify.htm
tech.root: offlinefiles
ms.assetid: 59bd7a71-0189-4c4d-a737-e6a3f09a533d

ms.date: 12/05/2018
ms.keywords: IOfflineFilesEvents3 interface [Offline Files],TransparentCacheItemNotify method, IOfflineFilesEvents3.TransparentCacheItemNotify, IOfflineFilesEvents3::TransparentCacheItemNotify, TransparentCacheItemNotify, TransparentCacheItemNotify method [Offline Files], TransparentCacheItemNotify method [Offline Files],IOfflineFilesEvents3 interface, cscobj/IOfflineFilesEvents3::TransparentCacheItemNotify, of.iofflinefilesevents3_transparentcacheitemnotify
ms.topic: method
f1_keywords: 
 - "cscobj/IOfflineFilesEvents3.TransparentCacheItemNotify"
dev_langs:
 - c++
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
 - IOfflineFilesEvents3.TransparentCacheItemNotify
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesEvents3::TransparentCacheItemNotify


## -description


Reports that an action has been performed on a transparently cached item.


## -parameters




### -param pszPath [in]

The item's UNC path string.


### -param EventType [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_events">OFFLINEFILES_EVENTS</a> enumeration value that indicates the type of the item.


### -param ItemType [in]

An <a href="https://docs.microsoft.com/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_item_type">OFFLINEFILES_ITEM_TYPE</a> enumeration value that indicates the type of the item.


### -param bModifiedData [in]

<b>TRUE</b> if the item's data was modified, <b>FALSE</b> otherwise.


### -param bModifiedAttributes [in]

<b>TRUE</b> if one or more of the item's attributes were modified, <b>FALSE</b> otherwise.


### -param pzsOldPath [in]

The original UNC path string for the item.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesevents3">IOfflineFilesEvents3</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilestransparentcacheinfo-istransparentlycached">IOfflineFilesTransparentCacheInfo::IsTransparentlyCached</a>
 

 

