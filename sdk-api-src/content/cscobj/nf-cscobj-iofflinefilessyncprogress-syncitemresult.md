---
UID: NF:cscobj.IOfflineFilesSyncProgress.SyncItemResult
title: IOfflineFilesSyncProgress::SyncItemResult (cscobj.h)
description: Reports that an item has been processed during the synchronization operation.
helpviewer_keywords: ["IOfflineFilesSyncProgress interface [Offline Files]","SyncItemResult method","IOfflineFilesSyncProgress.SyncItemResult","IOfflineFilesSyncProgress::SyncItemResult","SyncItemResult","SyncItemResult method [Offline Files]","SyncItemResult method [Offline Files]","IOfflineFilesSyncProgress interface","cscobj/IOfflineFilesSyncProgress::SyncItemResult","of.iofflinefilessyncprogress_syncitemresult"]
old-location: of\iofflinefilessyncprogress_syncitemresult.htm
tech.root: of
ms.assetid: 2a93d52e-6b91-4d91-9372-5f0718621841
ms.date: 12/05/2018
ms.keywords: IOfflineFilesSyncProgress interface [Offline Files],SyncItemResult method, IOfflineFilesSyncProgress.SyncItemResult, IOfflineFilesSyncProgress::SyncItemResult, SyncItemResult, SyncItemResult method [Offline Files], SyncItemResult method [Offline Files],IOfflineFilesSyncProgress interface, cscobj/IOfflineFilesSyncProgress::SyncItemResult, of.iofflinefilessyncprogress_syncitemresult
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
 - IOfflineFilesSyncProgress::SyncItemResult
 - cscobj/IOfflineFilesSyncProgress::SyncItemResult
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
 - IOfflineFilesSyncProgress.SyncItemResult
---

# IOfflineFilesSyncProgress::SyncItemResult


## -description

Reports that an item has been processed during the synchronization operation.  This method is called even if the operation was unsuccessful.  Check the value received in the <i>hrResult</i> parameter to determine whether the operation was successful.

## -parameters

### -param pszFile [in]

Receives the fully qualified UNC path of the item that was processed.

### -param hrResult [in]

Receives the result of the operation for the item.  Contains S_OK if the operation completed successfully or an error value otherwise.

### -param pErrorInfo [in]

Receives a pointer to an instance of the <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncerrorinfo">IOfflineFilesSyncErrorInfo</a> interface that provides detailed information about the result of the sync operation.

### -param pResponse [out]

Set this parameter to a value from the <a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_op_response">OFFLINEFILES_OP_RESPONSE</a> enumeration that indicates how the operation is to proceed.

## -returns

The return value is ignored.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessyncprogress">IOfflineFilesSyncProgress</a>