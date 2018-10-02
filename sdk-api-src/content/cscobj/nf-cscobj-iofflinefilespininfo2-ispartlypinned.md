---
UID: NF:cscobj.IOfflineFilesPinInfo2.IsPartlyPinned
title: IOfflineFilesPinInfo2::IsPartlyPinned
author: windows-sdk-content
description: Determines whether the item is partly pinned.
old-location: of\iofflinefilespininfo2_ispartlypinned.htm
tech.root: OfflineFiles
ms.assetid: 9063a804-2597-4959-8249-e5b42f582ea3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IOfflineFilesPinInfo2 interface [Offline Files],IsPartlyPinned method, IOfflineFilesPinInfo2.IsPartlyPinned, IOfflineFilesPinInfo2::IsPartlyPinned, IsPartlyPinned, IsPartlyPinned method [Offline Files], IsPartlyPinned method [Offline Files],IOfflineFilesPinInfo2 interface, cscobj/IOfflineFilesPinInfo2::IsPartlyPinned, of.iofflinefilespininfo2_ispartlypinned
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IOfflineFilesPinInfo2.IsPartlyPinned
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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




<a href="https://msdn.microsoft.com/6005d755-5e1b-4eba-95a2-b6c9c00b1a64">IOfflineFilesCache::Pin</a>



<a href="https://msdn.microsoft.com/b2e8ca73-4186-4971-b5be-41ecfc6b5e4a">IOfflineFilesGhostInfo::IsGhosted</a>



<a href="https://msdn.microsoft.com/80aa7e38-dbd7-42c6-b4b8-df4f104dfdc8">IOfflineFilesPinInfo2</a>



<a href="https://msdn.microsoft.com/7f8656e0-0f24-46a0-81b7-62067b0d4c21">IOfflineFilesTransparentCacheInfo::IsTransparentlyCached</a>
 

 

