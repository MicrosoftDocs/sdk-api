---
UID: NF:cscobj.IOfflineFilesTransparentCacheInfo.IsTransparentlyCached
title: IOfflineFilesTransparentCacheInfo::IsTransparentlyCached (cscobj.h)
description: Determines whether the item is transparently cached.
old-location: of\iofflinefilestransparentcacheinfo_istransparentlycached.htm
tech.root: offlinefiles
ms.assetid: 7f8656e0-0f24-46a0-81b7-62067b0d4c21
ms.date: 12/05/2018
ms.keywords: IOfflineFilesTransparentCacheInfo interface [Offline Files],IsTransparentlyCached method, IOfflineFilesTransparentCacheInfo.IsTransparentlyCached, IOfflineFilesTransparentCacheInfo::IsTransparentlyCached, IsTransparentlyCached, IsTransparentlyCached method [Offline Files], IsTransparentlyCached method [Offline Files],IOfflineFilesTransparentCacheInfo interface, cscobj/IOfflineFilesTransparentCacheInfo::IsTransparentlyCached, of.iofflinefilestransparentcacheinfo_istransparentlycached
ms.topic: method
f1_keywords:
- cscobj/IOfflineFilesTransparentCacheInfo.IsTransparentlyCached
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
- IOfflineFilesTransparentCacheInfo.IsTransparentlyCached
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesTransparentCacheInfo::IsTransparentlyCached


## -description


Determines whether the item is transparently cached.


## -parameters




### -param pbTransparentlyCached [out]

A pointer to a variable that receives <b>TRUE</b> if the item is transparently cached, or <b>FALSE</b> otherwise.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



A transparently cached item is cached locally. However, it can be accessed only when the server is available and the user is online with respect to that server. If the cached version of the file matches the currect version of the file on the server, requests to read data will be satisfied from the cache rather than requesting the data from the server.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesevents3-transparentcacheitemnotify">IOfflineFilesEvents3::TransparentCacheItemNotify</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilestransparentcacheinfo">IOfflineFilesTransparentCacheInfo</a>
 

 

