---
UID: NN:mobsync.ISyncMgrRegister
title: ISyncMgrRegister
author: windows-sdk-content
description: Exposes methods so that an application can register with the synchronization manager. This can be achieved either through the ISyncMgrRegister interface or by registering directly in the registry.
old-location: shell\syncmgr_isyncmgrregister.htm
tech.root: shell
ms.assetid: 1feed230-5a50-4ff5-a8a9-e0ce15ba8f1c
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: ISyncMgrRegister, ISyncMgrRegister interface [Windows Shell], ISyncMgrRegister interface [Windows Shell],described, mobsync/ISyncMgrRegister, shell.syncmgr_isyncmgrregister, syncmgr.isyncmgrregister
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mobsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mobsync.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mobsync.dll
api_name:
 - ISyncMgrRegister
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



