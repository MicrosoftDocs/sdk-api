---
UID: NN:mobsync.ISyncMgrSynchronize
title: ISyncMgrSynchronize (mobsync.h)
author: windows-sdk-content
description: Exposes methods that enable the registered application or service to receive notifications from the synchronization manager.
old-location: shell\syncmgr_isyncmgrsynchronize.htm
tech.root: shell
ms.assetid: bb821672-10b1-4fe6-a752-6cd1ccd1e49e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISyncMgrSynchronize, ISyncMgrSynchronize interface [Windows Shell], ISyncMgrSynchronize interface [Windows Shell],described, mobsync/ISyncMgrSynchronize, shell.syncmgr_isyncmgrsynchronize, syncmgr.isyncmgrsynchronize
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
 - ISyncMgrSynchronize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrSynchronize interface


## -description


Exposes methods that enable the registered application or service to receive notifications from the synchronization manager.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrSynchronize</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncMgrSynchronize</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrSynchronize</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75f6ce68-237f-4228-adcf-f5ec929f49a7">EnumSyncMgrItems</a>
</td>
<td align="left" width="63%">
Obtains the 
<a href="https://msdn.microsoft.com/d90e3a19-0ea8-4396-a6e7-dafe1dc9b2ec">ISyncMgrEnumItems</a> interface for the items that are handled by a registered application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bae3ead8-632c-45bf-a24e-bf07922039bd">GetHandlerInfo</a>
</td>
<td align="left" width="63%">
Obtains handler information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e21e1cd5-ab15-42e3-b3c7-1ae0c4dfec02">GetItemObject</a>
</td>
<td align="left" width="63%">
Obtains an interface on a specified item that a registered application handles.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4357d66e-b1f5-4a3c-b1a9-3a40aa6d8e10">Initialize</a>
</td>
<td align="left" width="63%">
Called by the synchronization manager in a registered application handler to determine whether the handler processes the synchronization event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">PrepareForSync</a>
</td>
<td align="left" width="63%">
Allows a registered application to display any user interface, and perform any necessary initialization before the <a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">ISyncMgrSynchronize::Synchronize</a> method is called. For example, an application such as the Outlook email client may need to display the password dialog box to enable a user to log on to a mail server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/311e916c-46a0-4eb2-a5e3-8da417ae7d71">SetItemStatus</a>
</td>
<td align="left" width="63%">
Called by the synchronization manager in a registered application's handler to change the status of an item in the following two cases: between the time the handler has returned from the <a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">ISyncMgrSynchronize::PrepareForSync</a> method and called the 
<a href="https://msdn.microsoft.com/2ba73e09-c01b-44af-8979-8aae450c9c0b">ISyncMgrSynchronizeCallback::PrepareForSyncCompleted</a> callback method, or after the handler has returned from the <a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">ISyncMgrSynchronize::Synchronize</a> method but has not yet called the <a href="https://msdn.microsoft.com/df0f0e20-6b84-4ff1-badb-40006a4b8e2c">ISyncMgrSynchronizeCallback::SynchronizeCompleted</a> callback method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/193926e8-824c-4969-9707-e2d95961c242">SetProgressCallback</a>
</td>
<td align="left" width="63%">
Sets the <a href="https://msdn.microsoft.com/1c817a21-be91-43af-86c8-aa7909ae2fa2">ISyncMgrSynchronizeCallback</a> interface. Registered applications use this callback interface to give status information from within the <a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">ISyncMgrSynchronize::PrepareForSync</a> and <a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">ISyncMgrSynchronize::Synchronize</a> methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e313c61-6482-4396-b4b8-824fba0226ac">ShowError</a>
</td>
<td align="left" width="63%">
Called by the synchronization manager in a registered application handler when a user double-clicks an associated message in the error tab.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5587cc8a-b359-483e-98ba-82f1bbe058d8">ShowProperties</a>
</td>
<td align="left" width="63%">
Called by the synchronization manager when a user selects an item in the choice dialog box, and then clicks the <b>Properties</b> button.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">Synchronize</a>
</td>
<td align="left" width="63%">
Called by the synchronization manager once for each selected group after the user has chosen the registered applications to be synchronized.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
This interface should be implemented on the registered application's handler to receive notifications from the synchronization manager and to participate in the synchronization process.

<b>ISyncMgrSynchronize</b> has been replaced in Windows Vista by <a href="https://msdn.microsoft.com/39579030-1cf5-4e82-a5e7-cb3415903d02">ISyncMgrHandler</a>.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
The synchronization manager calls the methods of this interface to send notifications to the registered application or service during synchronization.




## -see-also




<a href="https://msdn.microsoft.com/d90e3a19-0ea8-4396-a6e7-dafe1dc9b2ec">ISyncMgrEnumItems</a>



<a href="https://msdn.microsoft.com/1c817a21-be91-43af-86c8-aa7909ae2fa2">ISyncMgrSynchronizeCallback</a>



<a href="https://msdn.microsoft.com/993fd482-39e0-4966-ba71-eed7e4b54f72">ISyncMgrSynchronizeInvoke</a>
 

 

