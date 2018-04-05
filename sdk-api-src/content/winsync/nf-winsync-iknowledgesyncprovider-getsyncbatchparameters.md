---
UID: NF:winsync.IKnowledgeSyncProvider.GetSyncBatchParameters
title: IKnowledgeSyncProvider::GetSyncBatchParameters method
author: windows-driver-content
description: Gets the requested number of item changes that will be included in change batches, and the current knowledge for the synchronization scope.
old-location: winsync\iknowledgesyncprovider_getsyncbatchparameters.htm
old-project: winsync
ms.assetid: 25ebd3f7-8b62-44f3-83cd-c67c5e4f6617
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: GetSyncBatchParameters method [Windows Sync], GetSyncBatchParameters method [Windows Sync], IKnowledgeSyncProvider interface, GetSyncBatchParameters,IKnowledgeSyncProvider.GetSyncBatchParameters, IKnowledgeSyncProvider, IKnowledgeSyncProvider interface [Windows Sync], GetSyncBatchParameters method, IKnowledgeSyncProvider::GetSyncBatchParameters, winsync.iknowledgesyncprovider_getsyncbatchparameters, winsync/IKnowledgeSyncProvider::GetSyncBatchParameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	IKnowledgeSyncProvider.GetSyncBatchParameters
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IKnowledgeSyncProvider::GetSyncBatchParameters method


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




<a href="https://msdn.microsoft.com/396bbf7e-7fd0-4a2e-8304-f87097cd5e50">IKnowledgeSyncProvider Interface</a>
 

 

