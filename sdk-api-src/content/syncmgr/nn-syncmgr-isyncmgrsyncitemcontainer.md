---
UID: NN:syncmgr.ISyncMgrSyncItemContainer
title: ISyncMgrSyncItemContainer (syncmgr.h)
description: Exposes methods that provide information to handlers about the items they contain.
old-location: shell\ISyncMgrSyncItemContainer.htm
tech.root: shell
ms.assetid: c07487a5-aa12-411d-93bd-3774262e55c6
ms.date: 12/05/2018
ms.keywords: ISyncMgrSyncItemContainer, ISyncMgrSyncItemContainer interface [Windows Shell], ISyncMgrSyncItemContainer interface [Windows Shell],described, _shell_ISyncMgrSyncItemContainer, shell.ISyncMgrSyncItemContainer, syncmgr/ISyncMgrSyncItemContainer
f1_keywords:
- syncmgr/ISyncMgrSyncItemContainer
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
- ISyncMgrSyncItemContainer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrSyncItemContainer interface


## -description


Exposes methods that provide information to handlers about the items they contain.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrSyncItemContainer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrSyncItemContainer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrSyncItemContainer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitem">GetSyncItem</a>
</td>
<td align="left" width="63%">
Gets a specified sync item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitemcount">GetSyncItemCount</a>
</td>
<td align="left" width="63%">
Gets a count of the sync items in the container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitemenumerator">GetSyncItemEnumerator</a>
</td>
<td align="left" width="63%">
Gets an interface that enumerates the handler's sync items.

</td>
</tr>
</table> 


## -remarks



Sync Center calls <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrhandler">ISyncMgrHandler</a> interface to obtain a pointer to the <b>ISyncMgrSyncItemContainer</b> interface.



