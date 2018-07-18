---
UID: NN:syncmgr.ISyncMgrSyncItemContainer
title: ISyncMgrSyncItemContainer
author: windows-sdk-content
description: Exposes methods that provide information to handlers about the items they contain.
old-location: shell\ISyncMgrSyncItemContainer.htm
old-project: shell
ms.assetid: c07487a5-aa12-411d-93bd-3774262e55c6
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: ISyncMgrSyncItemContainer, ISyncMgrSyncItemContainer interface [Windows Shell], ISyncMgrSyncItemContainer interface [Windows Shell],described, _shell_ISyncMgrSyncItemContainer, shell.ISyncMgrSyncItemContainer, syncmgr/ISyncMgrSyncItemContainer
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
tech.root: 
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrSyncItemContainer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrSyncItemContainer interface


## -description


Exposes methods that provide information to handlers about the items they contain.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrSyncItemContainer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncMgrSyncItemContainer</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/27cdfcfe-d419-4232-b1cc-b9e7b8b2d315">GetSyncItem</a>
</td>
<td align="left" width="63%">
Gets a specified sync item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bbe37dff-d758-41ca-872d-4607d605011d">GetSyncItemCount</a>
</td>
<td align="left" width="63%">
Gets a count of the sync items in the container.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/761698b8-9531-440e-90f3-41b86f1cc674">GetSyncItemEnumerator</a>
</td>
<td align="left" width="63%">
Gets an interface that enumerates the handler's sync items.

</td>
</tr>
</table> 


## -remarks



Sync Center calls <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the <a href="https://msdn.microsoft.com/39579030-1cf5-4e82-a5e7-cb3415903d02">ISyncMgrHandler</a> interface to obtain a pointer to the <b>ISyncMgrSyncItemContainer</b> interface.



