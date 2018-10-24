---
UID: NN:syncmgr.IEnumSyncMgrSyncItems
title: IEnumSyncMgrSyncItems
author: windows-sdk-content
description: Exposes methods that enumerate the sync item objects managed by the handler.
old-location: shell\IEnumSyncMgrSyncItems.htm
tech.root: shell
ms.assetid: 0d1695e2-6936-4f53-9594-e0e2bc69afd4
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IEnumSyncMgrSyncItems, IEnumSyncMgrSyncItems interface [Windows Shell], IEnumSyncMgrSyncItems interface [Windows Shell],described, _shell_IEnumSyncMgrSyncItems, shell.IEnumSyncMgrSyncItems, syncmgr/IEnumSyncMgrSyncItems
ms.prod: windows
ms.technology: windows-sdk
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
 - IEnumSyncMgrSyncItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumSyncMgrSyncItems interface


## -description


Exposes methods that enumerate the sync item objects managed by the handler.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumSyncMgrSyncItems</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumSyncMgrSyncItems</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/bf320918-9f63-494f-88af-a5fab91ef0e3">Clone</a>
</td>
<td align="left" width="63%">
Not used. Clones an <b>IEnumSyncMgrSyncItems</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b886e3a8-a94b-45ed-893b-889bef70ae6a">Next</a>
</td>
<td align="left" width="63%">
Gets the next batch of sync items from the handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8144b47e-0419-4bc8-a57d-dc5c2b743f62">Reset</a>
</td>
<td align="left" width="63%">
Resets the current position in the enumeration to 0.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a07038de-84dc-4371-b72f-c835efd73ffc">Skip</a>
</td>
<td align="left" width="63%">
Skips forward in the enumeration the specified number of items.

</td>
</tr>
</table> 


## -remarks



A handler returns a pointer to an <b>IEnumSyncMgrSyncItems</b> interface from <a href="https://msdn.microsoft.com/761698b8-9531-440e-90f3-41b86f1cc674">ISyncMgrSyncItemContainer::GetSyncItemEnumerator</a>.



