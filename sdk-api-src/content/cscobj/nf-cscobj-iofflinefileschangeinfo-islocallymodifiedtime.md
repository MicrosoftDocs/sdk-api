---
UID: NF:cscobj.IOfflineFilesChangeInfo.IsLocallyModifiedTime
title: IOfflineFilesChangeInfo::IsLocallyModifiedTime (cscobj.h)
description: Determines whether one or more of an item's time values were modified while working offline.
helpviewer_keywords: ["IOfflineFilesChangeInfo interface [Offline Files]","IsLocallyModifiedTime method","IOfflineFilesChangeInfo.IsLocallyModifiedTime","IOfflineFilesChangeInfo::IsLocallyModifiedTime","IsLocallyModifiedTime","IsLocallyModifiedTime method [Offline Files]","IsLocallyModifiedTime method [Offline Files]","IOfflineFilesChangeInfo interface","cscobj/IOfflineFilesChangeInfo::IsLocallyModifiedTime","of.iofflinefileschangeinfo_islocallymodifiedtime"]
old-location: of\iofflinefileschangeinfo_islocallymodifiedtime.htm
tech.root: of
ms.assetid: 7b88bf6d-f5a7-48e3-8c0a-41a8f6fba91f
ms.date: 12/05/2018
ms.keywords: IOfflineFilesChangeInfo interface [Offline Files],IsLocallyModifiedTime method, IOfflineFilesChangeInfo.IsLocallyModifiedTime, IOfflineFilesChangeInfo::IsLocallyModifiedTime, IsLocallyModifiedTime, IsLocallyModifiedTime method [Offline Files], IsLocallyModifiedTime method [Offline Files],IOfflineFilesChangeInfo interface, cscobj/IOfflineFilesChangeInfo::IsLocallyModifiedTime, of.iofflinefileschangeinfo_islocallymodifiedtime
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
 - IOfflineFilesChangeInfo::IsLocallyModifiedTime
 - cscobj/IOfflineFilesChangeInfo::IsLocallyModifiedTime
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
 - IOfflineFilesChangeInfo.IsLocallyModifiedTime
---

# IOfflineFilesChangeInfo::IsLocallyModifiedTime


## -description

Determines whether one or more of an item's time values were modified while working offline.

## -parameters

### -param pbLocallyModifiedTime [out]

Receives <b>TRUE</b> if one or more of the item's time values were modified in the Offline Files cache while working offline, or <b>FALSE</b> otherwise.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

Use <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesfilesysinfo-gettimes">IOfflineFilesFileSysInfo::GetTimes</a> to examine the time values associated with an item.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefileschangeinfo">IOfflineFilesChangeInfo</a>