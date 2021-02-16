---
UID: NF:winsync.IKnowledgeSyncProvider.GetSyncBatchParameters
title: IKnowledgeSyncProvider::GetSyncBatchParameters (winsync.h)
description: Gets the requested number of item changes that will be included in change batches, and the current knowledge for the synchronization scope.
helpviewer_keywords: ["GetSyncBatchParameters","GetSyncBatchParameters method [Windows Sync]","GetSyncBatchParameters method [Windows Sync]","IKnowledgeSyncProvider interface","IKnowledgeSyncProvider interface [Windows Sync]","GetSyncBatchParameters method","IKnowledgeSyncProvider.GetSyncBatchParameters","IKnowledgeSyncProvider::GetSyncBatchParameters","winsync.iknowledgesyncprovider_getsyncbatchparameters","winsync/IKnowledgeSyncProvider::GetSyncBatchParameters"]
old-location: winsync\iknowledgesyncprovider_getsyncbatchparameters.htm
tech.root: winsync
ms.assetid: 25ebd3f7-8b62-44f3-83cd-c67c5e4f6617
ms.date: 12/05/2018
ms.keywords: GetSyncBatchParameters, GetSyncBatchParameters method [Windows Sync], GetSyncBatchParameters method [Windows Sync],IKnowledgeSyncProvider interface, IKnowledgeSyncProvider interface [Windows Sync],GetSyncBatchParameters method, IKnowledgeSyncProvider.GetSyncBatchParameters, IKnowledgeSyncProvider::GetSyncBatchParameters, winsync.iknowledgesyncprovider_getsyncbatchparameters, winsync/IKnowledgeSyncProvider::GetSyncBatchParameters
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKnowledgeSyncProvider::GetSyncBatchParameters
 - winsync/IKnowledgeSyncProvider::GetSyncBatchParameters
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IKnowledgeSyncProvider.GetSyncBatchParameters
---

# IKnowledgeSyncProvider::GetSyncBatchParameters


## -description

Gets the requested number of item changes that will be included in change batches, and the current knowledge for the synchronization scope.

## -parameters

### -param ppSyncKnowledge [out]

Returns the current knowledge for the synchronization scope, or a newly created knowledge object if no current knowledge exists.

### -param pdwRequestedBatchSize [out]

Returns the requested number of item changes that will be included in change batches returned by the source provider.

## -returns

The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Provider-determined error codes</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-iknowledgesyncprovider">IKnowledgeSyncProvider Interface</a>