---
UID: NF:cscobj.IOfflineFilesCache.SetDiskSpaceLimits
title: IOfflineFilesCache::SetDiskSpaceLimits
author: windows-sdk-content
description: Sets disk space usage limits on the Offline Files cache.
old-location: of\iofflinefilescache_setdiskspacelimits.htm
old-project: offlinefiles
ms.assetid: cdbfd5af-000a-4724-8a44-5641b2f75896
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IOfflineFilesCache interface [Offline Files],SetDiskSpaceLimits method, IOfflineFilesCache.SetDiskSpaceLimits, IOfflineFilesCache::SetDiskSpaceLimits, SetDiskSpaceLimits, SetDiskSpaceLimits method [Offline Files], SetDiskSpaceLimits method [Offline Files],IOfflineFilesCache interface, cscobj/IOfflineFilesCache::SetDiskSpaceLimits, of.iofflinefilescache_setdiskspacelimits
ms.prod: windows
ms.technology: windows-sdk
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
 - IOfflineFilesCache.SetDiskSpaceLimits
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesCache::SetDiskSpaceLimits


## -description


Sets disk space usage limits on the Offline Files cache.


## -parameters




### -param cbLimit [in]

Specifies the limit on the maximum amount of bytes that can be stored in the Offline Files cache.


### -param cbUnpinnedLimit [in]

Specifies the limit on the maximum amount of bytes that can be stored in the Offline Files cache for automatically cached files.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



The caller must be an administrator on the local machine.

The current disk space limits may be obtained by calling <a href="https://msdn.microsoft.com/94ea826a-bfc4-4010-a57f-c3a1af985d03">IOfflineFilesCache::GetDiskSpaceInformation</a>.




## -see-also




<a href="https://msdn.microsoft.com/7b1b5ef6-355a-4760-9d54-ec73cc66fb8a">IOfflineFilesCache</a>
 

 

