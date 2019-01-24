---
UID: NN:vsprov.IVssProviderCreateSnapshotSet
title: IVssProviderCreateSnapshotSet
author: windows-sdk-content
description: The IVssProviderCreateSnapshotSet interface contains the methods used during shadow copy creation.
old-location: base\ivssprovidercreatesnapshotset.htm
tech.root: VSS
ms.assetid: 41a795f0-7882-47a3-9226-aa50218a56e9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVssProviderCreateSnapshotSet, IVssProviderCreateSnapshotSet interface [VSS], IVssProviderCreateSnapshotSet interface [VSS],described, base.ivssprovidercreatesnapshotset, vsprov/IVssProviderCreateSnapshotSet
ms.topic: interface
req.header: vsprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsProv.h
api_name:
 - IVssProviderCreateSnapshotSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVssProviderCreateSnapshotSet interface


## -description


The <b>IVssProviderCreateSnapshotSet</b> 
   interface contains the methods used during shadow copy creation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssProviderCreateSnapshotSet</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVssProviderCreateSnapshotSet</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssProviderCreateSnapshotSet</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/393fd5aa-9934-4918-8699-25c41d0dc982">AbortSnapshots</a>
</td>
<td align="left" width="63%">
Ends the prepared shadow copies in this provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60489142-125f-4deb-afa0-9dae63ea1d46">CommitSnapshots</a>
</td>
<td align="left" width="63%">
Quickly commit all the LUNs in this provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/230666c7-e7e4-4e75-a84d-1786e8cbbb6c">EndPrepareSnapshots</a>
</td>
<td align="left" width="63%">
Ensure all LUNs in the shadow copy set are prepared.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/191b263b-1bcf-4617-95d4-5b4c1ed714ee">PostCommitSnapshots</a>
</td>
<td align="left" width="63%">
Called after all shadow copies have been committed, after the release-writes, before the 
     applications are unfrozen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3b6f7e6e-f1ea-4c90-9d26-fcbe5e104e2c">PostFinalCommitSnapshots</a>
</td>
<td align="left" width="63%">
Called after the writers have finished the auto-recovery of the components to allow the provider to make 
     any appropriate volumes read-only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af1caf80-751d-4b0d-8b35-970800d1dee6">PreCommitSnapshots</a>
</td>
<td align="left" width="63%">
Ensure the provider is ready to quickly commit the prepared LUNs. 
     This happens immediately before the flush-and-hold writes, but while applications are in a frozen state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d6895b9-6e6c-4c4c-b7c9-a4eff771567a">PreFinalCommitSnapshots</a>
</td>
<td align="left" width="63%">
Called after the applications are unfrozen to allow the writers to 
     <a href="https://msdn.microsoft.com/en-us/library/Aa384651(v=VS.85).aspx">auto-recover</a> any components so 
     that they can be used when they are read-only.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3a0c60df-666c-4e33-a54c-7fa5ddbfde13">Volume Shadow Copy API Interfaces</a>
 

 

