---
UID: NF:cscobj.IOfflineFilesSyncProgress.SyncItemBegin
title: IOfflineFilesSyncProgress::SyncItemBegin (cscobj.h)
description: Reports that a synchronization operation on an item is beginning.
helpviewer_keywords: ["IOfflineFilesSyncProgress interface [Offline Files]","SyncItemBegin method","IOfflineFilesSyncProgress.SyncItemBegin","IOfflineFilesSyncProgress::SyncItemBegin","SyncItemBegin","SyncItemBegin method [Offline Files]","SyncItemBegin method [Offline Files]","IOfflineFilesSyncProgress interface","cscobj/IOfflineFilesSyncProgress::SyncItemBegin","of.iofflinefilessyncprogress_syncitembegin"]
old-location: of\iofflinefilessyncprogress_syncitembegin.htm
tech.root: of
ms.assetid: c1cdbc30-bcc9-4023-a3a2-070fb9958609
ms.date: 12/05/2018
ms.keywords: IOfflineFilesSyncProgress interface [Offline Files],SyncItemBegin method, IOfflineFilesSyncProgress.SyncItemBegin, IOfflineFilesSyncProgress::SyncItemBegin, SyncItemBegin, SyncItemBegin method [Offline Files], SyncItemBegin method [Offline Files],IOfflineFilesSyncProgress interface, cscobj/IOfflineFilesSyncProgress::SyncItemBegin, of.iofflinefilessyncprogress_syncitembegin
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
 - IOfflineFilesSyncProgress::SyncItemBegin
 - cscobj/IOfflineFilesSyncProgress::SyncItemBegin
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
 - IOfflineFilesSyncProgress.SyncItemBegin
---

# IOfflineFilesSyncProgress::SyncItemBegin


## -description

Reports that a synchronization operation on an item is beginning.

## -parameters

### -param pszFile [in]

Receives the fully qualified UNC path of the file or directory to be processed.

### -param pResponse [out]

Your implementation of this method should set this parameter to a value from the <a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_op_response">OFFLINEFILES_OP_RESPONSE</a> enumeration that indicates how the operation is to proceed.

## -returns

The return value is ignored.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncprogress">IOfflineFilesSyncProgress</a>