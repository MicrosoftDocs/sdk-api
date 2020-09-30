---
UID: NF:cscobj.IOfflineFilesSyncErrorInfo.InfoEnumerated
title: IOfflineFilesSyncErrorInfo::InfoEnumerated (cscobj.h)
description: Indicates whether information was queried for the local, remote, or original copy of the item during synchronization.
helpviewer_keywords: ["IOfflineFilesSyncErrorInfo interface [Offline Files]","InfoEnumerated method","IOfflineFilesSyncErrorInfo.InfoEnumerated","IOfflineFilesSyncErrorInfo::InfoEnumerated","InfoEnumerated","InfoEnumerated method [Offline Files]","InfoEnumerated method [Offline Files]","IOfflineFilesSyncErrorInfo interface","cscobj/IOfflineFilesSyncErrorInfo::InfoEnumerated","of.iofflinefilessyncerrorinfo_infoenumerated"]
old-location: of\iofflinefilessyncerrorinfo_infoenumerated.htm
tech.root: of
ms.assetid: d2e8ae5b-92e7-4284-a02f-6eb3ab288376
ms.date: 12/05/2018
ms.keywords: IOfflineFilesSyncErrorInfo interface [Offline Files],InfoEnumerated method, IOfflineFilesSyncErrorInfo.InfoEnumerated, IOfflineFilesSyncErrorInfo::InfoEnumerated, InfoEnumerated, InfoEnumerated method [Offline Files], InfoEnumerated method [Offline Files],IOfflineFilesSyncErrorInfo interface, cscobj/IOfflineFilesSyncErrorInfo::InfoEnumerated, of.iofflinefilessyncerrorinfo_infoenumerated
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
 - IOfflineFilesSyncErrorInfo::InfoEnumerated
 - cscobj/IOfflineFilesSyncErrorInfo::InfoEnumerated
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
 - IOfflineFilesSyncErrorInfo.InfoEnumerated
---

# IOfflineFilesSyncErrorInfo::InfoEnumerated


## -description

Indicates whether information was queried for the local, remote, or original copy of the item during synchronization.

## -parameters

### -param pbLocalEnumerated [out]

Receives <b>TRUE</b> if information was queried for the local copy of the item during synchronization, or <b>FALSE</b> otherwise.

### -param pbRemoteEnumerated [out]

Receives <b>TRUE</b> if information was queried for the remote copy of the item during synchronization, or <b>FALSE</b> otherwise.

### -param pbOriginalEnumerated [out]

Receives <b>TRUE</b> if information was queried for the original copy of the item during synchronization, or <b>FALSE</b> otherwise.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncerrorinfo">IOfflineFilesSyncErrorInfo</a>