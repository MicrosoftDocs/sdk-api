---
UID: NN:syncmgr.IEnumSyncMgrSyncItems
title: IEnumSyncMgrSyncItems (syncmgr.h)
author: windows-sdk-content
description: Exposes methods that enumerate the sync item objects managed by the handler.
old-location: shell\IEnumSyncMgrSyncItems.htm
tech.root: shell
ms.assetid: 0d1695e2-6936-4f53-9594-e0e2bc69afd4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumSyncMgrSyncItems, IEnumSyncMgrSyncItems interface [Windows Shell], IEnumSyncMgrSyncItems interface [Windows Shell],described, _shell_IEnumSyncMgrSyncItems, shell.IEnumSyncMgrSyncItems, syncmgr/IEnumSyncMgrSyncItems
ms.topic: interface
f1_keywords: 
 - "syncmgr/IEnumSyncMgrSyncItems"
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
 - IEnumSyncMgrSyncItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumSyncMgrSyncItems interface


## -description


Exposes methods that enumerate the sync item objects managed by the handler.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumSyncMgrSyncItems</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumSyncMgrSyncItems</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumSyncMgrSyncItems</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-ienumsyncmgrsyncitems-clone">Clone</a>
</td>
<td align="left" width="63%">
Not used. Clones an <b>IEnumSyncMgrSyncItems</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-ienumsyncmgrsyncitems-next">Next</a>
</td>
<td align="left" width="63%">
Gets the next batch of sync items from the handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-ienumsyncmgrsyncitems-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the current position in the enumeration to 0.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-ienumsyncmgrsyncitems-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips forward in the enumeration the specified number of items.

</td>
</tr>
</table> 


## -remarks



A handler returns a pointer to an <b>IEnumSyncMgrSyncItems</b> interface from <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitemcontainer-getsyncitemenumerator">ISyncMgrSyncItemContainer::GetSyncItemEnumerator</a>.



