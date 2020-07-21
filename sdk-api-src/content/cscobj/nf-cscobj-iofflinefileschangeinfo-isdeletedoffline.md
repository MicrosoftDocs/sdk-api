---
UID: NF:cscobj.IOfflineFilesChangeInfo.IsDeletedOffline
title: IOfflineFilesChangeInfo::IsDeletedOffline (cscobj.h)
description: Determines whether an item has been deleted from the Offline Files cache while working offline.
helpviewer_keywords: ["IOfflineFilesChangeInfo interface [Offline Files]","IsDeletedOffline method","IOfflineFilesChangeInfo.IsDeletedOffline","IOfflineFilesChangeInfo::IsDeletedOffline","IsDeletedOffline","IsDeletedOffline method [Offline Files]","IsDeletedOffline method [Offline Files]","IOfflineFilesChangeInfo interface","cscobj/IOfflineFilesChangeInfo::IsDeletedOffline","of.iofflinefileschangeinfo_isdeletedoffline"]
old-location: of\iofflinefileschangeinfo_isdeletedoffline.htm
tech.root: offlinefiles
ms.assetid: c6a739f3-0c3d-46f1-8548-89be0660ef59
ms.date: 12/05/2018
ms.keywords: IOfflineFilesChangeInfo interface [Offline Files],IsDeletedOffline method, IOfflineFilesChangeInfo.IsDeletedOffline, IOfflineFilesChangeInfo::IsDeletedOffline, IsDeletedOffline, IsDeletedOffline method [Offline Files], IsDeletedOffline method [Offline Files],IOfflineFilesChangeInfo interface, cscobj/IOfflineFilesChangeInfo::IsDeletedOffline, of.iofflinefileschangeinfo_isdeletedoffline
f1_keywords:
- cscobj/IOfflineFilesChangeInfo.IsDeletedOffline
dev_langs:
- c++
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
- IOfflineFilesChangeInfo.IsDeletedOffline
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesChangeInfo::IsDeletedOffline


## -description


Determines whether an item has been deleted from the Offline Files cache while working offline.


## -parameters




### -param pbDeletedOffline [out]

Receives <b>TRUE</b> if the item has been deleted from the Offline Files cache while working offline, or <b>FALSE</b> otherwise.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefileschangeinfo">IOfflineFilesChangeInfo</a>
 

 

