---
UID: NN:syncmgr.ISyncMgrConflictItems
title: ISyncMgrConflictItems
author: windows-sdk-content
description: Exposes methods that get conflict item data and item count.
old-location: shell\ISyncMgrConflictItems.htm
old-project: shell
ms.assetid: 1dea310d-137b-4180-99c9-e40cd4fa3a98
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ISyncMgrConflictItems, ISyncMgrConflictItems interface [Windows Shell], ISyncMgrConflictItems interface [Windows Shell],described, _shell_ISyncMgrConflictItems, shell.ISyncMgrConflictItems, syncmgr/ISyncMgrConflictItems
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
 - ISyncMgrConflictItems
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrConflictItems interface


## -description


Exposes methods that get conflict item data and item count.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrConflictItems</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncMgrConflictItems</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrConflictItems</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597609">GetCount</a>
</td>
<td align="left" width="63%">
Gets the conflict item count.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f75a0cc5-1f82-426a-bb66-f34000219300">GetItem</a>
</td>
<td align="left" width="63%">
Gets a specified conflict data item.

</td>
</tr>
</table> 

