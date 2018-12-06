---
UID: NN:mobsync.ISyncMgrSynchronizeInvoke
title: ISyncMgrSynchronizeInvoke
author: windows-sdk-content
description: Exposes methods that enable a registered application to invoke the synchronization manager to update items.
old-location: shell\syncmgr_isyncmgrsynchronizeinvoke.htm
tech.root: shell
ms.assetid: 993fd482-39e0-4966-ba71-eed7e4b54f72
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISyncMgrSynchronizeInvoke, ISyncMgrSynchronizeInvoke interface [Windows Shell], ISyncMgrSynchronizeInvoke interface [Windows Shell],described, mobsync/ISyncMgrSynchronizeInvoke, shell.syncmgr_isyncmgrsynchronizeinvoke, syncmgr.isyncmgrsynchronizeinvoke
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ISyncMgrSynchronizeInvoke
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrSynchronizeInvoke interface


## -description


Exposes methods that enable a registered application to invoke the synchronization manager to update items.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrSynchronizeInvoke</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncMgrSynchronizeInvoke</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrSynchronizeInvoke</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94731c78-b7cf-4ad2-afe5-6355830a5550">UpdateAll</a>
</td>
<td align="left" width="63%">
Programmatically starts an update for all items.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a646d11-a84c-44c1-b52b-ffd364cc2ac3">UpdateItems</a>
</td>
<td align="left" width="63%">
Programmatically starts an update for specified items.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
This interface is implemented by the synchronization manager.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
A registered application calls the methods of this interface to update all items or to update specific items.



