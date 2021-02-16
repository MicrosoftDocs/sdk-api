---
UID: NF:cscobj.IOfflineFilesCache.EnumSettingObjects
title: IOfflineFilesCache::EnumSettingObjects (cscobj.h)
description: Creates an enumerator of instances of IOfflineFilesSetting.
helpviewer_keywords: ["EnumSettingObjects","EnumSettingObjects method [Offline Files]","EnumSettingObjects method [Offline Files]","IOfflineFilesCache interface","IOfflineFilesCache interface [Offline Files]","EnumSettingObjects method","IOfflineFilesCache.EnumSettingObjects","IOfflineFilesCache::EnumSettingObjects","cscobj/IOfflineFilesCache::EnumSettingObjects","of.iofflinefilescache_enumsettingobjects"]
old-location: of\iofflinefilescache_enumsettingobjects.htm
tech.root: of
ms.assetid: 1f2bb562-810a-4cc1-a072-eb870149954a
ms.date: 12/05/2018
ms.keywords: EnumSettingObjects, EnumSettingObjects method [Offline Files], EnumSettingObjects method [Offline Files],IOfflineFilesCache interface, IOfflineFilesCache interface [Offline Files],EnumSettingObjects method, IOfflineFilesCache.EnumSettingObjects, IOfflineFilesCache::EnumSettingObjects, cscobj/IOfflineFilesCache::EnumSettingObjects, of.iofflinefilescache_enumsettingobjects
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
 - IOfflineFilesCache::EnumSettingObjects
 - cscobj/IOfflineFilesCache::EnumSettingObjects
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
 - IOfflineFilesCache.EnumSettingObjects
---

# IOfflineFilesCache::EnumSettingObjects


## -description

Creates an enumerator of instances of <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessetting">IOfflineFilesSetting</a>. This allows the caller to enumerate all of the available settings that affect the behavior of Offline Files.

## -parameters

### -param ppEnum [out]

On success, receives the address of an instance of <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-ienumofflinefilessettings">IEnumOfflineFilesSettings</a>.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

A known setting may be retrieved by name using <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-getsettingobject">IOfflineFilesCache::GetSettingObject</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilescache">IOfflineFilesCache</a>