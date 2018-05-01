---
UID: NN:syncmgr.IEnumSyncMgrConflict
title: IEnumSyncMgrConflict
author: windows-driver-content
description: Exposes conflict enumeration methods.
old-location: shell\IEnumSyncMgrConflict.htm
old-project: shell
ms.assetid: 627f39be-5c9d-49a1-af73-210cdbb7940a
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IEnumSyncMgrConflict, IEnumSyncMgrConflict interface [Windows Shell], IEnumSyncMgrConflict interface [Windows Shell], described, _shell_IEnumSyncMgrConflict, shell.IEnumSyncMgrConflict, syncmgr/IEnumSyncMgrConflict
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
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Syncmgr.h
api_name:
-	IEnumSyncMgrConflict
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEnumSyncMgrConflict interface


## -description


Exposes conflict enumeration methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumSyncMgrConflict</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumSyncMgrConflict</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumSyncMgrConflict</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Not used. Clones an <b>IEnumSyncMgrConflict</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Gets the next batch of conflicts from the conflicts store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets the current position in the enumeration to zero.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a>
</td>
<td align="left" width="63%">
Skips forward the specified number of conflicts in the enumeration.

</td>
</tr>
</table> 


## -remarks



A conflict store returns a pointer to an <b>IEnumSyncMgrConflict</b> interface from <a href="https://msdn.microsoft.com/b59c679c-7759-4b7a-9a23-f054af99d6a7">ISyncMgrConflictStore::EnumConflicts</a>.



