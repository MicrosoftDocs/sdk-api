---
UID: NN:vss.IVssAsync
title: IVssAsync
author: windows-sdk-content
description: The IVssAsync interface is returned to calling applications by methods that initiate asynchronous operations, which run in the background and typically require a long time to complete.
old-location: base\ivssasync.htm
tech.root: vss
ms.assetid: d2cff547-b4ff-454d-8e0e-cd29b91cbb07
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IVssAsync, IVssAsync interface [VSS], IVssAsync interface [VSS],described, _win32_ivssasync, base.ivssasync, vss/IVssAsync
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: vss.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: VssApi.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssAsync
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssAsync interface


## -description


The <b>IVssAsync</b> interface is returned to calling applications 
    by methods that initiate asynchronous operations, which run in the background and typically require a long time 
    to complete.

The <b>IVssAsync</b> interface permits an application to monitor and 
    control an asynchronous operation by waiting on its completion, querying its status, or canceling it.

The calling application is responsible for calling <a href="_com_iunknown_release">IUnknown::Release</a> to release the 
    resources held by the returned <b>IVssAsync</b> interface when it is 
    no longer needed.

The following methods return an <b>IVssAsync</b> interface:
<ul>
<li>
<a href="https://msdn.microsoft.com/ee49d4b1-f3f4-4c85-a3a2-f4452d066f21">IVssBackupComponents::BackupComplete</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3cc6c375-8a24-4af3-b4ad-5a695cc2645c">IVssBackupComponents::DoSnapshotSet</a>
</li>
<li>
<a href="https://msdn.microsoft.com/44f19c10-c966-4ab6-98dd-865d535955db">IVssBackupComponents::GatherWriterMetadata</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ca87cdc3-e233-4efc-81c0-918e5a698af5">IVssBackupComponents::GatherWriterStatus</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7f28c841-5448-4ed7-b76e-0aa5376fd8bf">IVssBackupComponents::ImportSnapshots</a>
</li>
<li>
<a href="https://msdn.microsoft.com/01cf3931-59ef-4572-9f2e-aa210da0ac2d">IVssBackupComponents::PostRestore</a>
</li>
<li>
<a href="https://msdn.microsoft.com/46ce8282-a434-4b0b-b66e-40810052b34b">IVssBackupComponents::PrepareForBackup</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7a4c8869-9655-49a7-818b-98a08103f4b4">IVssBackupComponents::PreRestore</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssAsync</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVssAsync</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssAsync</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ab44737-114b-4edc-a097-d0fa297f6276">Cancel</a>
</td>
<td align="left" width="63%">
Cancels an incomplete asynchronous operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85fb3ae8-dc09-4f6f-a96b-e4dc046ff48a">QueryStatus</a>
</td>
<td align="left" width="63%">
Queries the status of an asynchronous operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27be3bb2-de37-47d1-a2da-7b253ace1199">Wait</a>
</td>
<td align="left" width="63%">
Waits until an incomplete asynchronous operation will be finished, and the operation's completion status.

</td>
</tr>
</table> 

