---
UID: NF:cscobj.IOfflineFilesCache.EnumSettingObjects
title: IOfflineFilesCache::EnumSettingObjects
author: windows-driver-content
description: Creates an enumerator of instances of IOfflineFilesSetting.
old-location: of\iofflinefilescache_enumsettingobjects.htm
old-project: OfflineFiles
ms.assetid: 1f2bb562-810a-4cc1-a072-eb870149954a
ms.author: windowsdriverdev
ms.date: 5/9/2018
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
req.typenames: OFFLINEFILES_SYNC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CscSvc.dll
-	CscObj.dll
api_name:
-	IOfflineFilesCache.EnumSettingObjects
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesCache::EnumSettingObjects


## -description



    Creates an enumerator of instances of <a href="https://msdn.microsoft.com/6f47c67b-9438-4229-89b2-6b3f9da8fb68">IOfflineFilesSetting</a>. This allows the caller to enumerate all of the available settings that affect the behavior of Offline Files.


## -parameters




### -param ppEnum [out]

On success, receives the address of an instance of <a href="https://msdn.microsoft.com/2d0e45d5-5559-4c2e-9c20-4e5b84b5fbbd">IEnumOfflineFilesSettings</a>.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



A known setting may be retrieved by name using <a href="https://msdn.microsoft.com/17b6572d-f05e-4f0e-a247-89acd2963d6b">IOfflineFilesCache::GetSettingObject</a>.




## -see-also




<a href="https://msdn.microsoft.com/7b1b5ef6-355a-4760-9d54-ec73cc66fb8a">IOfflineFilesCache</a>
 

 

