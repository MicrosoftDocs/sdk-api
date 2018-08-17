---
UID: NF:cscobj.IOfflineFilesPinInfo2.IsPartlyPinned
title: IOfflineFilesPinInfo2::IsPartlyPinned
author: windows-sdk-content
description: Determines whether the item is partly pinned.
old-location: of\iofflinefilespininfo2_ispartlypinned.htm
old-project: offlinefiles
ms.assetid: 9063a804-2597-4959-8249-e5b42f582ea3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOfflineFilesPinInfo2 interface [Offline Files],IsPartlyPinned method, IOfflineFilesPinInfo2.IsPartlyPinned, IOfflineFilesPinInfo2::IsPartlyPinned, IsPartlyPinned, IsPartlyPinned method [Offline Files], IsPartlyPinned method [Offline Files],IOfflineFilesPinInfo2 interface, cscobj/IOfflineFilesPinInfo2::IsPartlyPinned, of.iofflinefilespininfo2_ispartlypinned
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: cscobj.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: OFFLINEFILES_SYNC_STATE
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
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
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




<a href="https://msdn.microsoft.com/en-us/library/Bb530498(v=VS.85).aspx">IOfflineFilesCache::Pin</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd941690(v=VS.85).aspx">IOfflineFilesGhostInfo::IsGhosted</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd941691(v=VS.85).aspx">IOfflineFilesPinInfo2</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd442651(v=VS.85).aspx">IOfflineFilesTransparentCacheInfo::IsTransparentlyCached</a>
 

 

