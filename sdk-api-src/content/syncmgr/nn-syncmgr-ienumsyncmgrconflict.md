---
UID: NN:syncmgr.IEnumSyncMgrConflict
title: IEnumSyncMgrConflict
author: windows-sdk-content
description: Exposes conflict enumeration methods.
old-location: shell\IEnumSyncMgrConflict.htm
tech.root: shell
ms.assetid: 627f39be-5c9d-49a1-af73-210cdbb7940a
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IEnumSyncMgrConflict, IEnumSyncMgrConflict interface [Windows Shell], IEnumSyncMgrConflict interface [Windows Shell],described, _shell_IEnumSyncMgrConflict, shell.IEnumSyncMgrConflict, syncmgr/IEnumSyncMgrConflict
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
 - IEnumSyncMgrConflict
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/2eb0f1c1-71e2-45e6-bef7-1b480efb4ab7">Clone</a>
</td>
<td align="left" width="63%">
Not used. Clones an <b>IEnumSyncMgrConflict</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/486fba93-cdd1-49fd-96a8-cf56d1775a7c">Next</a>
</td>
<td align="left" width="63%">
Gets the next batch of conflicts from the conflicts store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58dece75-8fc3-42ae-89c8-407ebeaa7efb">Reset</a>
</td>
<td align="left" width="63%">
Resets the current position in the enumeration to zero.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d636dd60-835f-40a8-b2e6-7d7ebf87e897">Skip</a>
</td>
<td align="left" width="63%">
Skips forward the specified number of conflicts in the enumeration.

</td>
</tr>
</table> 


## -remarks



A conflict store returns a pointer to an <b>IEnumSyncMgrConflict</b> interface from <a href="https://msdn.microsoft.com/b59c679c-7759-4b7a-9a23-f054af99d6a7">ISyncMgrConflictStore::EnumConflicts</a>.



