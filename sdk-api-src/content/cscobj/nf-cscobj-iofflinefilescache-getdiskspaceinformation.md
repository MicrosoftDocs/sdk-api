---
UID: NF:cscobj.IOfflineFilesCache.GetDiskSpaceInformation
title: IOfflineFilesCache::GetDiskSpaceInformation
author: windows-sdk-content
description: Retrieves the amount of disk space used by the Offline Files cache as well as the space limits applied to cache usage.
old-location: of\iofflinefilescache_getdiskspaceinformation.htm
old-project: offlinefiles
ms.assetid: 94ea826a-bfc4-4010-a57f-c3a1af985d03
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetDiskSpaceInformation, GetDiskSpaceInformation method [Offline Files], GetDiskSpaceInformation method [Offline Files],IOfflineFilesCache interface, IOfflineFilesCache interface [Offline Files],GetDiskSpaceInformation method, IOfflineFilesCache.GetDiskSpaceInformation, IOfflineFilesCache::GetDiskSpaceInformation, cscobj/IOfflineFilesCache::GetDiskSpaceInformation, of.iofflinefilescache_getdiskspaceinformation
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
 - IOfflineFilesCache.GetDiskSpaceInformation
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesCache::GetDiskSpaceInformation


## -description


Retrieves the amount of disk space used by the Offline Files cache as well as the space limits applied to cache usage.


## -parameters




### -param pcbVolumeTotal [out]

Receives the size, in bytes, of the volume hosting the Offline Files cache.


### -param pcbLimit [out]

Receives the limit on the maximum amount of bytes that can be stored in the Offline Files cache.


### -param pcbUsed [out]

Receives the current number of bytes used by all files that are pinned and automatically cached in the Offline Files cache.


### -param pcbUnpinnedLimit [out]

Receives the limit on the maximum amount of bytes that can be stored in the Offline Files cache for automatically cached files.


### -param pcbUnpinnedUsed [out]

Receives the current number of bytes used by all automatically cached files in the Offline Files cache.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



The cache space limits may be adjusted by an administrator using <a href="https://msdn.microsoft.com/cdbfd5af-000a-4724-8a44-5641b2f75896">IOfflineFilesCache::SetDiskSpaceLimits</a>.




## -see-also




<a href="https://msdn.microsoft.com/7b1b5ef6-355a-4760-9d54-ec73cc66fb8a">IOfflineFilesCache</a>
 

 

