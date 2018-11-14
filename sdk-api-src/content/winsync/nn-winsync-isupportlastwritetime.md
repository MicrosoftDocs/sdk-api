---
UID: NN:winsync.ISupportLastWriteTime
title: ISupportLastWriteTime
author: windows-sdk-content
description: Represents a synchronization provider that is able to report the date and time when an item or change unit was last changed. This ability is useful to an application that implements last-writer-wins conflict resolution.
old-location: winsync\isupportlastwritetime.htm
tech.root: winsync
ms.assetid: b95e2b75-add7-4cdd-b18a-21918e9c8c08
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ISupportLastWriteTime, ISupportLastWriteTime interface [Windows Sync], ISupportLastWriteTime interface [Windows Sync],described, winsync.isupportlastwritetime, winsync/ISupportLastWriteTime
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISupportLastWriteTime
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISupportLastWriteTime interface


## -description


Represents a synchronization provider that is able to report the date and time when an item or change unit was last changed. This ability is useful to an application that implements last-writer-wins conflict resolution.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISupportLastWriteTime</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISupportLastWriteTime</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISupportLastWriteTime</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f289d5a5-c991-4223-b59a-68b31ecffb8c">GetChangeUnitChangeTime</a>
</td>
<td align="left" width="63%">
Gets the date and time when the specified change unit was last changed.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15cbd398-81d9-4ea6-bfe4-1bf00510b419">GetItemChangeTime</a>
</td>
<td align="left" width="63%">
Gets the date and time when the specified item was last changed.


</td>
</tr>
</table> 


## -remarks



This interface is typically implemented by a provider. If a provider implements this interface, it must return a pointer to it when <b>IID_ISupportLastWriteTime</b> is passed to the <b>QueryInterface</b> method of its data transfer interface. The data transfer interface is the interface that a provider returns in response to the <a href="https://msdn.microsoft.com/ae309301-3810-4785-b4f2-a55fbdf819d8">ISynchronousDataRetriever::LoadChangeData</a> method.

To implement last-writer-wins conflict resolution, an application typically performs the following steps:

<ol>
<li>Registers an <a href="https://msdn.microsoft.com/f6c96e02-e9db-402c-8197-580f688b068f">ISyncCallback</a> object to receive conflict notifications.</li>
<li>In the <a href="https://msdn.microsoft.com/439f2a73-b36c-4604-b739-9f9b68275ac5">ISyncCallback::OnConflict</a> method, calls <a href="https://msdn.microsoft.com/7a63d554-56e0-4c39-94ea-613fecc97331">IChangeConflict::GetDestinationProviderConflictingData</a> and <a href="https://msdn.microsoft.com/4227b559-59e9-4b87-beb0-2d47f3d81414">IChangeConflict::GetSourceProviderConflictingData</a> on the <a href="https://msdn.microsoft.com/b0089d3d-a1e6-4662-9e79-4c0b22c08d7f">IChangeConflict</a> object to get the data transfer interfaces for the conflicting changes.</li>
<li>Passes <b>IID_ISupportLastWriteTime</b> to the <b>QueryInterface</b> method of each data transfer interface to get the <b>ISupportLastWriteTime</b> objects that represent the conflicting changes.</li>
<li>Calls <a href="https://msdn.microsoft.com/15cbd398-81d9-4ea6-bfe4-1bf00510b419">GetItemChangeTime</a> or <a href="https://msdn.microsoft.com/f289d5a5-c991-4223-b59a-68b31ecffb8c">GetChangeUnitChangeTime</a> on the <b>ISupportLastWriteTime</b> objects to get the last date and time the changes were made.</li>
<li>Compares the date and time values to determine which change was made last.</li>
<li>Indicates which change to keep by using the <a href="https://msdn.microsoft.com/f1a26c85-a00d-408e-96ea-5849c6bb99ff">IChangeConflict::SetResolveActionForChange</a> or <a href="https://msdn.microsoft.com/8594a888-21a1-4cfb-964c-9c670e3a7438">IChangeConflict::SetResolveActionForChangeUnit</a> method.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/b0089d3d-a1e6-4662-9e79-4c0b22c08d7f">IChangeConflict Interface</a>



<a href="https://msdn.microsoft.com/f6c96e02-e9db-402c-8197-580f688b068f">ISyncCallback Interface</a>



<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

