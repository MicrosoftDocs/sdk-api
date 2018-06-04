---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ISyncMgrRegister interface


## -description


Exposes methods so that an application can register with the synchronization manager. This can be achieved either through the 
<b>ISyncMgrRegister</b> interface or by registering directly in the registry.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrRegister</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncMgrRegister</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrRegister</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35241829-58b8-448a-ae69-1d43b4d0ba10">GetHandlerRegistrationInfo</a>
</td>
<td align="left" width="63%">
Called by the registered application's handler to get current registration information.
   

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c980c57-90a1-4f97-8d0c-22a3abdefabb">RegisterSyncMgrHandler</a>
</td>
<td align="left" width="63%">
Registers a handler with the synchronization manager when the handler has items to synchronize.
      

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd823d73-a07a-4c75-a29c-6c48ad2c23dc">UnregisterSyncMgrHandler</a>
</td>
<td align="left" width="63%">
Removes a handler's CLSID from the registration. A handler should call this when it no longer has any items to synchronize.

</td>
</tr>
</table> 


## -remarks



The handler must be a standard OLE server. It must register the standard OLE keys for an InProc OLE server in addition to the SyncMgr key.



