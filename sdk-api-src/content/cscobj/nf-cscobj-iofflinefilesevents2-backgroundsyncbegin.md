---
UID: NF:cscobj.IOfflineFilesEvents2.BackgroundSyncBegin
title: IOfflineFilesEvents2::BackgroundSyncBegin (cscobj.h)
description: Reports that the Offline Files service is beginning to perform a background synchronization pass.
helpviewer_keywords: ["BackgroundSyncBegin","BackgroundSyncBegin method [Offline Files]","BackgroundSyncBegin method [Offline Files]","IOfflineFilesEvents2 interface","IOfflineFilesEvents2 interface [Offline Files]","BackgroundSyncBegin method","IOfflineFilesEvents2.BackgroundSyncBegin","IOfflineFilesEvents2::BackgroundSyncBegin","cscobj/IOfflineFilesEvents2::BackgroundSyncBegin","of.iofflinefilesevents2_backgroundsyncbegin"]
old-location: of\iofflinefilesevents2_backgroundsyncbegin.htm
tech.root: of
ms.assetid: 84b71228-904a-4042-8d13-422ae77f7ba5
ms.date: 12/05/2018
ms.keywords: BackgroundSyncBegin, BackgroundSyncBegin method [Offline Files], BackgroundSyncBegin method [Offline Files],IOfflineFilesEvents2 interface, IOfflineFilesEvents2 interface [Offline Files],BackgroundSyncBegin method, IOfflineFilesEvents2.BackgroundSyncBegin, IOfflineFilesEvents2::BackgroundSyncBegin, cscobj/IOfflineFilesEvents2::BackgroundSyncBegin, of.iofflinefilesevents2_backgroundsyncbegin
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
 - IOfflineFilesEvents2::BackgroundSyncBegin
 - cscobj/IOfflineFilesEvents2::BackgroundSyncBegin
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
 - IOfflineFilesEvents2.BackgroundSyncBegin
---

# IOfflineFilesEvents2::BackgroundSyncBegin


## -description

Reports that the Offline Files service is beginning to perform a background synchronization pass.

## -parameters

### -param dwSyncControlFlags [in]

One or more OFFLINEFILES_SYNC_CONTROL_FLAG_XXXXXX flags describing the purpose of the sync operation.  These may be used to determine if the sync is a one-way or two-way sync. These flags are described in the <i>dwSyncControl</i> parameter of the <a href="/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilescache-synchronize">IOfflineFilesCache::Synchronize</a> method.

## -returns

The return value is ignored.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesevents2">IOfflineFilesEvents2</a>