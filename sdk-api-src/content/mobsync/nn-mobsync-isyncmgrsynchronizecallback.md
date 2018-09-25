---
UID: NN:mobsync.ISyncMgrSynchronizeCallback
title: ISyncMgrSynchronizeCallback
author: windows-sdk-content
description: Exposes methods that manage the synchronization process.
old-location: shell\syncmgr_isyncmgrsynchronizecallback.htm
tech.root: shell
ms.assetid: 1c817a21-be91-43af-86c8-aa7909ae2fa2
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ISyncMgrSynchronizeCallback, ISyncMgrSynchronizeCallback interface [Windows Shell], ISyncMgrSynchronizeCallback interface [Windows Shell],described, mobsync/ISyncMgrSynchronizeCallback, shell.syncmgr_isyncmgrsynchronizecallback, syncmgr.isyncmgrsynchronizecallback
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
 - ISyncMgrSynchronizeCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrSynchronizeCallback interface


## -description


Exposes methods that manage the synchronization process.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrSynchronizeCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncMgrSynchronizeCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrSynchronizeCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06e90b81-14cc-4b3e-9d2d-30e60eeb8eb2">DeleteLogError</a>
</td>
<td align="left" width="63%">
Called by the registered application's handler to delete a previously logged ErrorInformation, warning, or error message in the error tab on the synchronization manager status dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00102220-3734-40f2-ae6c-2807e44e17a1">EnableModeless</a>
</td>
<td align="left" width="63%">
Called by the registered application before and after any dialog boxes are displayed from within the <a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">ISyncMgrSynchronize::PrepareForSync</a> and 
<a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">ISyncMgrSynchronize::Synchronize</a> methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7d1aff8-a77e-4067-9fc9-4adc69bfc0d1">EstablishConnection</a>
</td>
<td align="left" width="63%">
Called by the registered application's handler when a network connection is required.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c25ef21-9815-41ad-bcc0-b41a62dc0fe5">LogError</a>
</td>
<td align="left" width="63%">
Called by a registered application to log information, warning, or an error message into the error tab on the synchronization manager status dialog box.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ba73e09-c01b-44af-8979-8aae450c9c0b">PrepareForSyncCompleted</a>
</td>
<td align="left" width="63%">
Called by a registered handler of an application after the 
<a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">ISyncMgrSynchronize::PrepareForSync</a> method is complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/924310aa-e210-476d-b532-f235de943498">Progress</a>
</td>
<td align="left" width="63%">
Called by a registered application to update the progress information and determine whether an operation should continue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7441f8d3-1b9b-400f-a2c4-ec67f7677a32">ShowErrorCompleted</a>
</td>
<td align="left" width="63%">
Called by the registered application's handler before or after its <a href="https://msdn.microsoft.com/82e70e75-a5d4-41b2-87c4-2a032628954d">ISyncMgrSynchronize::PrepareForSync</a> operation has been completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d451e72e-d4a8-4899-b18e-d8912d817de5">ShowPropertiesCompleted</a>
</td>
<td align="left" width="63%">
Called by the registered application's handler before or after its 
<a href="https://msdn.microsoft.com/5587cc8a-b359-483e-98ba-82f1bbe058d8">ISyncMgrSynchronize::ShowProperties</a> operation is completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df0f0e20-6b84-4ff1-badb-40006a4b8e2c">SynchronizeCompleted</a>
</td>
<td align="left" width="63%">
Called by an application when its <a href="https://msdn.microsoft.com/78c202dd-9f8c-43c1-a7be-48030bc34a9c">ISyncMgrSynchronize::Synchronize</a> method is complete.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
This interface is implemented by the synchronization manager to receive status, error, and progress information and display the user interface during the synchronization process.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Applications should call the methods of this interface as often as possible and must call it before starting each new ItemID to check whether the user has canceled an individual item.




## -see-also




<a href="https://msdn.microsoft.com/bb821672-10b1-4fe6-a752-6cd1ccd1e49e">ISyncMgrSynchronize</a>
 

 

