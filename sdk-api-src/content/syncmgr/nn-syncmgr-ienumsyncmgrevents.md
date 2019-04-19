---
UID: NN:syncmgr.IEnumSyncMgrEvents
title: IEnumSyncMgrEvents (syncmgr.h)
author: windows-sdk-content
description: Exposes sync event enumeration methods.
old-location: shell\IEnumSyncMgrEvents.htm
tech.root: shell
ms.assetid: 74d0c373-e9b1-4d9c-bdb6-caa743938e32
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumSyncMgrEvents, IEnumSyncMgrEvents interface [Windows Shell], IEnumSyncMgrEvents interface [Windows Shell],described, _shell_IEnumSyncMgrEvents, shell.IEnumSyncMgrEvents, syncmgr/IEnumSyncMgrEvents
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
 - IEnumSyncMgrEvents
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumSyncMgrEvents interface


## -description


Exposes sync event enumeration methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumSyncMgrEvents</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumSyncMgrEvents</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/55be3dd4-993e-4f8f-a9d3-be5b7e4f6ddb">Clone</a>
</td>
<td align="left" width="63%">
Clones an <b>IEnumSyncMgrEvents</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22151b04-f4b8-46af-b55a-1ac2054900d3">Next</a>
</td>
<td align="left" width="63%">
Gets the next batch of events from the event store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/68c99781-aedf-4676-bbd2-ab6cc14bba46">Reset</a>
</td>
<td align="left" width="63%">
Resets the current location in the enumeration to zero.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e8257e8-fab3-407c-a6d0-26a7a9ca0961">Skip</a>
</td>
<td align="left" width="63%">
Skips forward the specified number of events in the enumeration.

</td>
</tr>
</table> 


## -remarks



An event store returns a pointer to an <b>IEnumSyncMgrEvents</b> interface from <a href="https://msdn.microsoft.com/8b634811-cb6d-47b2-b534-1baea23a5297">ISyncMgrEventStore::GetEventEnumerator</a>.



