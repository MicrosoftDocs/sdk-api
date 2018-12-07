---
UID: NN:syncmgr.ISyncMgrSyncCallback
title: ISyncMgrSyncCallback
author: windows-sdk-content
description: Exposes methods that allow a synchronization process to report progress and events to Sync Center, or to query whether the process has been canceled.
old-location: shell\ISyncMgrSyncCallback.htm
tech.root: shell
ms.assetid: 4f2b6dc3-3b81-4c0a-b0a2-b48f13fba397
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISyncMgrSyncCallback, ISyncMgrSyncCallback interface [Windows Shell], ISyncMgrSyncCallback interface [Windows Shell],described, _shell_ISyncMgrSyncCallback, shell.ISyncMgrSyncCallback, syncmgr/ISyncMgrSyncCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrSyncCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrSyncCallback interface


## -description


Exposes methods that allow a synchronization process to report progress and events to Sync Center, or to query whether the process has been canceled.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrSyncCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncMgrSyncCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrSyncCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1de3d6c0-cdf8-48fa-b7ff-2dc75f6757fc">AddItemToSession</a>
</td>
<td align="left" width="63%">
Adds a specified item to the set of items currently being synchronized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02106b6f-4c1c-4bd6-b120-2948b1e6d25c">CanContinue</a>
</td>
<td align="left" width="63%">
Determines whether the synchronization has been canceled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0964cd3-42ad-4af0-90b2-0f365f457448">CommitItem</a>
</td>
<td align="left" width="63%">
Confirms a specified item as a member of the handler's sync set and confirms that it should be shown in the UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0c73950-f80e-4831-9c56-4316561a269b">ProposeItem</a>
</td>
<td align="left" width="63%">
Proposes the addition of a new item to the set of items previously enumerated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3780d88a-4430-4cf3-9d1c-35eb8efc8971">QueryForAdditionalItems</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator of the set of items that have a pending request to be synchronized. This is the set of items that will be synchronized once the current synchronization is finished.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c7d6627-1652-4920-9dce-a61673e6e656">ReportEvent</a>
</td>
<td align="left" width="63%">
Provides an event to add to the Sync Results folder for an item being synchronized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e503f8f-ebfa-4ac9-a6de-e9127919c758">ReportManualSync</a>
</td>
<td align="left" width="63%">
Reports that a synchronization operation is being performed that was requested manually from outside the Sync Center UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd7ed6f4-49c6-44c7-86f9-0b2c04d19de8">ReportProgress</a>
</td>
<td align="left" width="63%">
Reports the progress of the synchronization of a single sync item to Sync Center.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f16de5e-fed0-4d2c-a764-2239f9225cad">SetHandlerProgressText</a>
</td>
<td align="left" width="63%">
Sets the content of an information field for the handler while that handler is performing a synchronization.

</td>
</tr>
</table> 


## -remarks



This interface is passed to <a href="https://msdn.microsoft.com/d1df43b6-406c-4da0-89f0-a17e51101520">ISyncMgrSessionCreator::CreateSession</a>, which in turn is referenced in the call to <a href="https://msdn.microsoft.com/6742f6a8-eda8-4ef0-8a11-dc70baefcc83">ISyncMgrHandler::Synchronize</a>.

The handler is expected to call this interface to update the folder's progress UI  for each item and to notify Sync Center when it has completed the synchronization of each item.

<b>ISyncMgrSyncCallback</b> is a replacement for <a href="https://msdn.microsoft.com/1c817a21-be91-43af-86c8-aa7909ae2fa2">ISyncMgrSynchronizeCallback</a>.



