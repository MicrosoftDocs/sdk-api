---
UID: NN:syncmgr.IEnumSyncMgrEvents
title: IEnumSyncMgrEvents (syncmgr.h)
description: Exposes sync event enumeration methods.
helpviewer_keywords: ["IEnumSyncMgrEvents","IEnumSyncMgrEvents interface [Windows Shell]","IEnumSyncMgrEvents interface [Windows Shell]","described","_shell_IEnumSyncMgrEvents","shell.IEnumSyncMgrEvents","syncmgr/IEnumSyncMgrEvents"]
old-location: shell\IEnumSyncMgrEvents.htm
tech.root: shell
ms.assetid: 74d0c373-e9b1-4d9c-bdb6-caa743938e32
ms.date: 12/05/2018
ms.keywords: IEnumSyncMgrEvents, IEnumSyncMgrEvents interface [Windows Shell], IEnumSyncMgrEvents interface [Windows Shell],described, _shell_IEnumSyncMgrEvents, shell.IEnumSyncMgrEvents, syncmgr/IEnumSyncMgrEvents
f1_keywords:
- syncmgr/IEnumSyncMgrEvents
dev_langs:
- c++
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
- IEnumSyncMgrEvents
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumSyncMgrEvents interface


## -description


Exposes sync event enumeration methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumSyncMgrEvents</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumSyncMgrEvents</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumSyncMgrEvents</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-ienumsyncmgrevents-clone">Clone</a>
</td>
<td align="left" width="63%">
Clones an <b>IEnumSyncMgrEvents</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-ienumsyncmgrevents-next">Next</a>
</td>
<td align="left" width="63%">
Gets the next batch of events from the event store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-ienumsyncmgrevents-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the current location in the enumeration to zero.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-ienumsyncmgrevents-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips forward the specified number of events in the enumeration.

</td>
</tr>
</table> 


## -remarks



An event store returns a pointer to an <b>IEnumSyncMgrEvents</b> interface from <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgreventstore-geteventenumerator">ISyncMgrEventStore::GetEventEnumerator</a>.



