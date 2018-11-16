---
UID: NF:cscobj.IOfflineFilesCache.EnumSettingObjects
title: IOfflineFilesCache::EnumSettingObjects
author: windows-sdk-content
description: Creates an enumerator of instances of IOfflineFilesSetting.
old-location: of\iofflinefilescache_enumsettingobjects.htm
tech.root: OfflineFiles
ms.assetid: 1f2bb562-810a-4cc1-a072-eb870149954a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: EnumSettingObjects, EnumSettingObjects method [Offline Files], EnumSettingObjects method [Offline Files],IOfflineFilesCache interface, IOfflineFilesCache interface [Offline Files],EnumSettingObjects method, IOfflineFilesCache.EnumSettingObjects, IOfflineFilesCache::EnumSettingObjects, cscobj/IOfflineFilesCache::EnumSettingObjects, of.iofflinefilescache_enumsettingobjects
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
 - IOfflineFilesCache.EnumSettingObjects
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
- IOfflineFilesCache.EnumSettingObjects
: 
---

# IOfflineFilesCache::EnumSettingObjects


## -description


Creates an enumerator of instances of <a href="https://msdn.microsoft.com/en-us/library/Bb530601(v=VS.85).aspx">IOfflineFilesSetting</a>. This allows the caller to enumerate all of the available settings that affect the behavior of Offline Files.


## -parameters




### -param ppEnum [out]

On success, receives the address of an instance of <a href="https://msdn.microsoft.com/en-us/library/Bb530481(v=VS.85).aspx">IEnumOfflineFilesSettings</a>.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



A known setting may be retrieved by name using <a href="https://msdn.microsoft.com/en-us/library/Bb530496(v=VS.85).aspx">IOfflineFilesCache::GetSettingObject</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530486(v=VS.85).aspx">IOfflineFilesCache</a>
 

 

