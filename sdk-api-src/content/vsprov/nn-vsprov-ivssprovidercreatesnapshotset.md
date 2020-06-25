---
UID: NN:vsprov.IVssProviderCreateSnapshotSet
title: IVssProviderCreateSnapshotSet (vsprov.h)
description: The IVssProviderCreateSnapshotSet interface contains the methods used during shadow copy creation.
helpviewer_keywords: ["IVssProviderCreateSnapshotSet","IVssProviderCreateSnapshotSet interface [VSS]","IVssProviderCreateSnapshotSet interface [VSS]","described","base.ivssprovidercreatesnapshotset","vsprov/IVssProviderCreateSnapshotSet"]
old-location: base\ivssprovidercreatesnapshotset.htm
tech.root: VSS
ms.assetid: 41a795f0-7882-47a3-9226-aa50218a56e9
ms.date: 12/05/2018
ms.keywords: IVssProviderCreateSnapshotSet, IVssProviderCreateSnapshotSet interface [VSS], IVssProviderCreateSnapshotSet interface [VSS],described, base.ivssprovidercreatesnapshotset, vsprov/IVssProviderCreateSnapshotSet
f1_keywords:
- vsprov/IVssProviderCreateSnapshotSet
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVssProviderCreateSnapshotSet interface


## -description


The <b>IVssProviderCreateSnapshotSet</b> 
   interface contains the methods used during shadow copy creation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssProviderCreateSnapshotSet</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IVssProviderCreateSnapshotSet</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivssprovidercreatesnapshotset-abortsnapshots">AbortSnapshots</a>
</td>
<td align="left" width="63%">
Ends the prepared shadow copies in this provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots">CommitSnapshots</a>
</td>
<td align="left" width="63%">
Quickly commit all the LUNs in this provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots">EndPrepareSnapshots</a>
</td>
<td align="left" width="63%">
Ensure all LUNs in the shadow copy set are prepared.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots">PostCommitSnapshots</a>
</td>
<td align="left" width="63%">
Called after all shadow copies have been committed, after the release-writes, before the 
     applications are unfrozen.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivssprovidercreatesnapshotset-postfinalcommitsnapshots">PostFinalCommitSnapshots</a>
</td>
<td align="left" width="63%">
Called after the writers have finished the auto-recovery of the components to allow the provider to make 
     any appropriate volumes read-only.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots">PreCommitSnapshots</a>
</td>
<td align="left" width="63%">
Ensure the provider is ready to quickly commit the prepared LUNs. 
     This happens immediately before the flush-and-hold writes, but while applications are in a frozen state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/vsprov/nf-vsprov-ivssprovidercreatesnapshotset-prefinalcommitsnapshots">PreFinalCommitSnapshots</a>
</td>
<td align="left" width="63%">
Called after the applications are unfrozen to allow the writers to 
     <a href="https://docs.microsoft.com/windows/desktop/VSS/vssgloss-a">auto-recover</a> any components so 
     that they can be used when they are read-only.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VSS/volume-shadow-copy-api-interfaces">Volume Shadow Copy API Interfaces</a>
 

 

