---
UID: NF:cscobj.IOfflineFilesSimpleProgress.ItemResult
title: IOfflineFilesSimpleProgress::ItemResult (cscobj.h)
description: Reports that an item has been processed during the operation.
helpviewer_keywords: ["IOfflineFilesSimpleProgress interface [Offline Files]","ItemResult method","IOfflineFilesSimpleProgress.ItemResult","IOfflineFilesSimpleProgress::ItemResult","ItemResult","ItemResult method [Offline Files]","ItemResult method [Offline Files]","IOfflineFilesSimpleProgress interface","cscobj/IOfflineFilesSimpleProgress::ItemResult","of.iofflinefilessimpleprogress_itemresult"]
old-location: of\iofflinefilessimpleprogress_itemresult.htm
tech.root: of
ms.assetid: 60ed3b12-b56e-4a58-8e37-a4a745ddb783
ms.date: 12/05/2018
ms.keywords: IOfflineFilesSimpleProgress interface [Offline Files],ItemResult method, IOfflineFilesSimpleProgress.ItemResult, IOfflineFilesSimpleProgress::ItemResult, ItemResult, ItemResult method [Offline Files], ItemResult method [Offline Files],IOfflineFilesSimpleProgress interface, cscobj/IOfflineFilesSimpleProgress::ItemResult, of.iofflinefilessimpleprogress_itemresult
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
 - IOfflineFilesSimpleProgress::ItemResult
 - cscobj/IOfflineFilesSimpleProgress::ItemResult
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
 - IOfflineFilesSimpleProgress.ItemResult
---

# IOfflineFilesSimpleProgress::ItemResult


## -description

Reports that an item has been processed during the operation.  This method is called even if the operation was unsuccessful.  Check the value received in the <i>hrResult</i> parameter to determine whether the operation was successful.

## -parameters

### -param pszFile [in]

Receives the fully qualified UNC path of the item that was processed.

### -param hrResult [in]

Receives the result of the operation for the item.  Contains S_OK if the operation completed successfully or an error value otherwise.

### -param pResponse [out]

Set this parameter to a value from the <a href="/windows/desktop/api/cscobj/ne-cscobj-offlinefiles_op_response">OFFLINEFILES_OP_RESPONSE</a> enumeration that indicates how the operation is to proceed.

## -returns

The return value is ignored.

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilessimpleprogress">IOfflineFilesSimpleProgress</a>