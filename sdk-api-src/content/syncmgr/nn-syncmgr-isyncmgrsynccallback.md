---
UID: NN:syncmgr.ISyncMgrSyncCallback
title: ISyncMgrSyncCallback (syncmgr.h)
description: Exposes methods that allow a synchronization process to report progress and events to Sync Center, or to query whether the process has been canceled.
helpviewer_keywords: ["ISyncMgrSyncCallback","ISyncMgrSyncCallback interface [Windows Shell]","ISyncMgrSyncCallback interface [Windows Shell]","described","_shell_ISyncMgrSyncCallback","shell.ISyncMgrSyncCallback","syncmgr/ISyncMgrSyncCallback"]
old-location: shell\ISyncMgrSyncCallback.htm
tech.root: shell
ms.assetid: 4f2b6dc3-3b81-4c0a-b0a2-b48f13fba397
ms.date: 12/05/2018
ms.keywords: ISyncMgrSyncCallback, ISyncMgrSyncCallback interface [Windows Shell], ISyncMgrSyncCallback interface [Windows Shell],described, _shell_ISyncMgrSyncCallback, shell.ISyncMgrSyncCallback, syncmgr/ISyncMgrSyncCallback
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncMgrSyncCallback
 - syncmgr/ISyncMgrSyncCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrSyncCallback
---

# ISyncMgrSyncCallback interface


## -description

Exposes methods that allow a synchronization process to report progress and events to Sync Center, or to query whether the process has been canceled.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrSyncCallback</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrSyncCallback</b> also has these types of members:
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
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynccallback-additemtosession">AddItemToSession</a>
</td>
<td align="left" width="63%">
Adds a specified item to the set of items currently being synchronized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynccallback-cancontinue">CanContinue</a>
</td>
<td align="left" width="63%">
Determines whether the synchronization has been canceled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynccallback-commititem">CommitItem</a>
</td>
<td align="left" width="63%">
Confirms a specified item as a member of the handler's sync set and confirms that it should be shown in the UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynccallback-proposeitem">ProposeItem</a>
</td>
<td align="left" width="63%">
Proposes the addition of a new item to the set of items previously enumerated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynccallback-queryforadditionalitems">QueryForAdditionalItems</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator of the set of items that have a pending request to be synchronized. This is the set of items that will be synchronized once the current synchronization is finished.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynccallback-reportevent">ReportEvent</a>
</td>
<td align="left" width="63%">
Provides an event to add to the Sync Results folder for an item being synchronized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynccallback-reportmanualsync">ReportManualSync</a>
</td>
<td align="left" width="63%">
Reports that a synchronization operation is being performed that was requested manually from outside the Sync Center UI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynccallback-reportprogress">ReportProgress</a>
</td>
<td align="left" width="63%">
Reports the progress of the synchronization of a single sync item to Sync Center.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsynccallback-sethandlerprogresstext">SetHandlerProgressText</a>
</td>
<td align="left" width="63%">
Sets the content of an information field for the handler while that handler is performing a synchronization.

</td>
</tr>
</table>

## -remarks

This interface is passed to <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsessioncreator-createsession">ISyncMgrSessionCreator::CreateSession</a>, which in turn is referenced in the call to <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-synchronize">ISyncMgrHandler::Synchronize</a>.

The handler is expected to call this interface to update the folder's progress UI  for each item and to notify Sync Center when it has completed the synchronization of each item.

<b>ISyncMgrSyncCallback</b> is a replacement for <a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronizecallback">ISyncMgrSynchronizeCallback</a>.