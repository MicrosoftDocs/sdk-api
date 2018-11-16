---
UID: NF:cscobj.IOfflineFilesPinInfo.IsPinnedForUserByPolicy
title: IOfflineFilesPinInfo::IsPinnedForUserByPolicy
author: windows-sdk-content
description: Determines whether the item was pinned for users by Group Policy.
old-location: of\iofflinefilespininfo_ispinnedforuserbypolicy.htm
tech.root: OfflineFiles
ms.assetid: fa5548e9-0a4e-4e66-a5ea-45d092c239b2
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IOfflineFilesPinInfo interface [Offline Files],IsPinnedForUserByPolicy method, IOfflineFilesPinInfo.IsPinnedForUserByPolicy, IOfflineFilesPinInfo::IsPinnedForUserByPolicy, IsPinnedForUserByPolicy, IsPinnedForUserByPolicy method [Offline Files], IsPinnedForUserByPolicy method [Offline Files],IOfflineFilesPinInfo interface, cscobj/IOfflineFilesPinInfo::IsPinnedForUserByPolicy, of.iofflinefilespininfo_ispinnedforuserbypolicy
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
 - IOfflineFilesPinInfo.IsPinnedForUserByPolicy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- cscobj.h
: 
- IOfflineFilesPinInfo.IsPinnedForUserByPolicy
: 
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

This method corresponds to the OFFLINEFILES_PIN_CONTROL_FLAG_FORUSER_POLICY pin control flag used by the <a href="https://msdn.microsoft.com/6005d755-5e1b-4eba-95a2-b6c9c00b1a64">IOfflineFilesCache::Pin</a> method.




## -see-also




<a href="https://msdn.microsoft.com/6005d755-5e1b-4eba-95a2-b6c9c00b1a64">IOfflineFilesCache::Pin</a>



<a href="https://msdn.microsoft.com/529a529a-fbeb-4414-b4c9-46bfcca4aa7a">IOfflineFilesPinInfo</a>
 

 

