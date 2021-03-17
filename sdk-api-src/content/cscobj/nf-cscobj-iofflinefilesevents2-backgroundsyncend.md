---
UID: NF:cscobj.IOfflineFilesEvents2.BackgroundSyncEnd
title: IOfflineFilesEvents2::BackgroundSyncEnd (cscobj.h)
description: Reports that the Offline Files service completed a background synchronization pass.
helpviewer_keywords: ["BackgroundSyncEnd","BackgroundSyncEnd method [Offline Files]","BackgroundSyncEnd method [Offline Files]","IOfflineFilesEvents2 interface","IOfflineFilesEvents2 interface [Offline Files]","BackgroundSyncEnd method","IOfflineFilesEvents2.BackgroundSyncEnd","IOfflineFilesEvents2::BackgroundSyncEnd","cscobj/IOfflineFilesEvents2::BackgroundSyncEnd","of.iofflinefilesevents2_backgroundsyncend"]
old-location: of\iofflinefilesevents2_backgroundsyncend.htm
tech.root: of
ms.assetid: d41a2152-8100-47a7-a994-a0fe9fae4dc4
ms.date: 12/05/2018
ms.keywords: BackgroundSyncEnd, BackgroundSyncEnd method [Offline Files], BackgroundSyncEnd method [Offline Files],IOfflineFilesEvents2 interface, IOfflineFilesEvents2 interface [Offline Files],BackgroundSyncEnd method, IOfflineFilesEvents2.BackgroundSyncEnd, IOfflineFilesEvents2::BackgroundSyncEnd, cscobj/IOfflineFilesEvents2::BackgroundSyncEnd, of.iofflinefilesevents2_backgroundsyncend
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
 - IOfflineFilesEvents2::BackgroundSyncEnd
 - cscobj/IOfflineFilesEvents2::BackgroundSyncEnd
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
 - IOfflineFilesEvents2.BackgroundSyncEnd
---

# IOfflineFilesEvents2::BackgroundSyncEnd


## -description

Reports that the Offline Files service completed a background synchronization pass.

## -parameters

### -param dwSyncControlFlags [in]

One or more OFFLINEFILES_SYNC_CONTROL_FLAG_XXXXXX flags describing the purpose of the sync operation.  These may be used to determine if the sync is a one-way or two-way sync. These flags are described in the <i>dwSyncControl</i> parameter of the <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-synchronize">IOfflineFilesCache::Synchronize</a> method.

## -returns

The return value is ignored.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesevents2">IOfflineFilesEvents2</a>