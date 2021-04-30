---
UID: NF:cscobj.IOfflineFilesChangeInfo.IsCreatedOffline
title: IOfflineFilesChangeInfo::IsCreatedOffline (cscobj.h)
description: Determines whether an item was created in the Offline Files cache while working offline.
helpviewer_keywords: ["IOfflineFilesChangeInfo interface [Offline Files]","IsCreatedOffline method","IOfflineFilesChangeInfo.IsCreatedOffline","IOfflineFilesChangeInfo::IsCreatedOffline","IsCreatedOffline","IsCreatedOffline method [Offline Files]","IsCreatedOffline method [Offline Files]","IOfflineFilesChangeInfo interface","cscobj/IOfflineFilesChangeInfo::IsCreatedOffline","of.iofflinefileschangeinfo_iscreatedoffline"]
old-location: of\iofflinefileschangeinfo_iscreatedoffline.htm
tech.root: of
ms.assetid: 2074df23-a2dd-45ea-9ef4-5619cebebe31
ms.date: 12/05/2018
ms.keywords: IOfflineFilesChangeInfo interface [Offline Files],IsCreatedOffline method, IOfflineFilesChangeInfo.IsCreatedOffline, IOfflineFilesChangeInfo::IsCreatedOffline, IsCreatedOffline, IsCreatedOffline method [Offline Files], IsCreatedOffline method [Offline Files],IOfflineFilesChangeInfo interface, cscobj/IOfflineFilesChangeInfo::IsCreatedOffline, of.iofflinefileschangeinfo_iscreatedoffline
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
 - IOfflineFilesChangeInfo::IsCreatedOffline
 - cscobj/IOfflineFilesChangeInfo::IsCreatedOffline
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
 - IOfflineFilesChangeInfo.IsCreatedOffline
---

# IOfflineFilesChangeInfo::IsCreatedOffline


## -description

Determines whether an item was created in the Offline Files cache while working offline.

## -parameters

### -param pbCreatedOffline [out]

Receives <b>TRUE</b> if the item was created in the Offline Files cache while working offline, or <b>FALSE</b> otherwise.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefileschangeinfo">IOfflineFilesChangeInfo</a>