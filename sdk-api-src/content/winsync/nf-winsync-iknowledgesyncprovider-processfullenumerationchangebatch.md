---
UID: NF:winsync.IKnowledgeSyncProvider.ProcessFullEnumerationChangeBatch
title: IKnowledgeSyncProvider::ProcessFullEnumerationChangeBatch (winsync.h)
description: Processes a set of changes for a full enumeration by applying changes to the item store.
helpviewer_keywords: ["IKnowledgeSyncProvider interface [Windows Sync]","ProcessFullEnumerationChangeBatch method","IKnowledgeSyncProvider.ProcessFullEnumerationChangeBatch","IKnowledgeSyncProvider::ProcessFullEnumerationChangeBatch","ProcessFullEnumerationChangeBatch","ProcessFullEnumerationChangeBatch method [Windows Sync]","ProcessFullEnumerationChangeBatch method [Windows Sync]","IKnowledgeSyncProvider interface","winsync.iknowledgesyncprovider_processfullenumerationchangebatch","winsync/IKnowledgeSyncProvider::ProcessFullEnumerationChangeBatch"]
old-location: winsync\iknowledgesyncprovider_processfullenumerationchangebatch.htm
tech.root: winsync
ms.assetid: 7d34bc48-377c-4249-a26e-0802dee0b53c
ms.date: 12/05/2018
ms.keywords: IKnowledgeSyncProvider interface [Windows Sync],ProcessFullEnumerationChangeBatch method, IKnowledgeSyncProvider.ProcessFullEnumerationChangeBatch, IKnowledgeSyncProvider::ProcessFullEnumerationChangeBatch, ProcessFullEnumerationChangeBatch, ProcessFullEnumerationChangeBatch method [Windows Sync], ProcessFullEnumerationChangeBatch method [Windows Sync],IKnowledgeSyncProvider interface, winsync.iknowledgesyncprovider_processfullenumerationchangebatch, winsync/IKnowledgeSyncProvider::ProcessFullEnumerationChangeBatch
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
 - IKnowledgeSyncProvider::ProcessFullEnumerationChangeBatch
 - winsync/IKnowledgeSyncProvider::ProcessFullEnumerationChangeBatch
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
 - IKnowledgeSyncProvider.ProcessFullEnumerationChangeBatch
---

# IKnowledgeSyncProvider::ProcessFullEnumerationChangeBatch


## -description

Processes a set of changes for a full enumeration by applying changes to the item store.

## -parameters

### -param resolutionPolicy [in]

The conflict resolution policy to use when this method applies changes.

### -param pSourceChangeBatch [in]

A batch of changes from the source provider to be applied locally.

### -param pUnkDataRetriever [in]

An object that can be used to retrieve change data. It can be an <b>ISynchronousDataRetriever</b> object or a provider-specific object.

### -param pCallback [in]

An object that receives event notifications during change application.

### -param pSyncSessionStatistics [in, out]

Tracks change statistics. For a provider that uses custom change application, this object must be updated with the results of the change application.

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

## -remarks

This method is called during forgotten knowledge recovery.

## -see-also

<a href="/windows/win32/api/winsync/ne-winsync-conflict_resolution_policy">CONFLICT RESOLUTION POLICY Enumeration</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-iknowledgesyncprovider">IKnowledgeSyncProvider Interface</a>



<a href="/windows/desktop/api/winsync/ns-winsync-sync_range">SYNC RANGE Structure</a>