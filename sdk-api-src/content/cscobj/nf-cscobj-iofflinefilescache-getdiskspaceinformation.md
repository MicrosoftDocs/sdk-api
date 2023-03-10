---
UID: NF:cscobj.IOfflineFilesCache.GetDiskSpaceInformation
title: IOfflineFilesCache::GetDiskSpaceInformation (cscobj.h)
description: Retrieves the amount of disk space used by the Offline Files cache as well as the space limits applied to cache usage.
helpviewer_keywords: ["GetDiskSpaceInformation","GetDiskSpaceInformation method [Offline Files]","GetDiskSpaceInformation method [Offline Files]","IOfflineFilesCache interface","IOfflineFilesCache interface [Offline Files]","GetDiskSpaceInformation method","IOfflineFilesCache.GetDiskSpaceInformation","IOfflineFilesCache::GetDiskSpaceInformation","cscobj/IOfflineFilesCache::GetDiskSpaceInformation","of.iofflinefilescache_getdiskspaceinformation"]
old-location: of\iofflinefilescache_getdiskspaceinformation.htm
tech.root: of
ms.assetid: 94ea826a-bfc4-4010-a57f-c3a1af985d03
ms.date: 12/05/2018
ms.keywords: GetDiskSpaceInformation, GetDiskSpaceInformation method [Offline Files], GetDiskSpaceInformation method [Offline Files],IOfflineFilesCache interface, IOfflineFilesCache interface [Offline Files],GetDiskSpaceInformation method, IOfflineFilesCache.GetDiskSpaceInformation, IOfflineFilesCache::GetDiskSpaceInformation, cscobj/IOfflineFilesCache::GetDiskSpaceInformation, of.iofflinefilescache_getdiskspaceinformation
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
 - IOfflineFilesCache::GetDiskSpaceInformation
 - cscobj/IOfflineFilesCache::GetDiskSpaceInformation
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
 - IOfflineFilesCache.GetDiskSpaceInformation
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

The cache space limits may be adjusted by an administrator using <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-setdiskspacelimits">IOfflineFilesCache::SetDiskSpaceLimits</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilescache">IOfflineFilesCache</a>