---
UID: NF:vsprov.IVssProviderCreateSnapshotSet.PostCommitSnapshots
title: IVssProviderCreateSnapshotSet::PostCommitSnapshots (vsprov.h)
description: Is called after all providers involved in the shadow copy set have succeeded with CommitSnapshots.
helpviewer_keywords: ["IVssProviderCreateSnapshotSet interface [VSS]","PostCommitSnapshots method","IVssProviderCreateSnapshotSet.PostCommitSnapshots","IVssProviderCreateSnapshotSet::PostCommitSnapshots","PostCommitSnapshots","PostCommitSnapshots method [VSS]","PostCommitSnapshots method [VSS]","IVssProviderCreateSnapshotSet interface","base.ivssprovidercreatesnapshotset_postcommitsnapshots","vsprov/IVssProviderCreateSnapshotSet::PostCommitSnapshots"]
old-location: base\ivssprovidercreatesnapshotset_postcommitsnapshots.htm
tech.root: base
ms.assetid: 191b263b-1bcf-4617-95d4-5b4c1ed714ee
ms.date: 12/05/2018
ms.keywords: IVssProviderCreateSnapshotSet interface [VSS],PostCommitSnapshots method, IVssProviderCreateSnapshotSet.PostCommitSnapshots, IVssProviderCreateSnapshotSet::PostCommitSnapshots, PostCommitSnapshots, PostCommitSnapshots method [VSS], PostCommitSnapshots method [VSS],IVssProviderCreateSnapshotSet interface, base.ivssprovidercreatesnapshotset_postcommitsnapshots, vsprov/IVssProviderCreateSnapshotSet::PostCommitSnapshots
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssProviderCreateSnapshotSet::PostCommitSnapshots
 - vsprov/IVssProviderCreateSnapshotSet::PostCommitSnapshots
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsProv.h
api_name:
 - IVssProviderCreateSnapshotSet.PostCommitSnapshots
---

# IVssProviderCreateSnapshotSet::PostCommitSnapshots


## -description

The <b>PostCommitSnapshots</b> 
   method is called after all providers involved in the shadow copy set have succeeded with 
   <a href="/windows/desktop/api/vsprov/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots">CommitSnapshots</a>. 
   The lock on the I/O system has been lifted, but the applications have not yet been unfrozen. This is an 
   opportunity for the provider to perform additional cleanup work after the shadow copy commit.

## -parameters

### -param SnapshotSetId [in]

The <b>VSS_ID</b> that identifies the shadow copy set.

### -param lSnapshotsCount [in]

Count of shadow copies in the shadow copy set.

## -returns

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
The operation was successfully completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
<dt>0x8007000EL</dt>
</dl>
</td>
<td width="60%">
Out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057L</dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_NOT_FOUND</b></dt>
<dt>0x80042308L</dt>
</dl>
</td>
<td width="60%">
The <i>SnapshotSetId</i> parameter refers to an object that was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
<dt>0x80042306L</dt>
</dl>
</td>
<td width="60%">
An unexpected provider error occurred. If this is returned, the error must be described in an entry in 
        the application event log, giving the user information on how to resolve the problem.

</td>
</tr>
</table>
 

If any other value is returned, VSS will write an event to the event log and convert the error to 
      <b>VSS_E_UNEXPECTED_PROVIDER_ERROR</b>.

## -see-also

<a href="/windows/desktop/api/vsprov/nn-vsprov-ivssprovidercreatesnapshotset">IVssProviderCreateSnapshotSet</a>