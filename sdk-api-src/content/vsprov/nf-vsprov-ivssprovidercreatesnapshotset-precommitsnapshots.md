---
UID: NF:vsprov.IVssProviderCreateSnapshotSet.PreCommitSnapshots
title: IVssProviderCreateSnapshotSet::PreCommitSnapshots (vsprov.h)
description: Ensures the provider is ready to quickly commit the prepared LUNs.
helpviewer_keywords: ["IVssProviderCreateSnapshotSet interface [VSS]","PreCommitSnapshots method","IVssProviderCreateSnapshotSet.PreCommitSnapshots","IVssProviderCreateSnapshotSet::PreCommitSnapshots","PreCommitSnapshots","PreCommitSnapshots method [VSS]","PreCommitSnapshots method [VSS]","IVssProviderCreateSnapshotSet interface","base.ivssprovidercreatesnapshotset_precommitsnapshots","vsprov/IVssProviderCreateSnapshotSet::PreCommitSnapshots"]
old-location: base\ivssprovidercreatesnapshotset_precommitsnapshots.htm
tech.root: base
ms.assetid: af1caf80-751d-4b0d-8b35-970800d1dee6
ms.date: 12/05/2018
ms.keywords: IVssProviderCreateSnapshotSet interface [VSS],PreCommitSnapshots method, IVssProviderCreateSnapshotSet.PreCommitSnapshots, IVssProviderCreateSnapshotSet::PreCommitSnapshots, PreCommitSnapshots, PreCommitSnapshots method [VSS], PreCommitSnapshots method [VSS],IVssProviderCreateSnapshotSet interface, base.ivssprovidercreatesnapshotset_precommitsnapshots, vsprov/IVssProviderCreateSnapshotSet::PreCommitSnapshots
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
 - IVssProviderCreateSnapshotSet::PreCommitSnapshots
 - vsprov/IVssProviderCreateSnapshotSet::PreCommitSnapshots
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
 - IVssProviderCreateSnapshotSet.PreCommitSnapshots
---

# IVssProviderCreateSnapshotSet::PreCommitSnapshots


## -description

The <b>PreCommitSnapshots</b> 
   method ensures the provider is ready to quickly commit the prepared LUNs. This happens 
   immediately before the flush-and-hold writes, but while applications are in a frozen state. During this call the 
   provider should prepare all shadow copies in the shadow copy set indicated by <i>SnapshotSetId</i> 
   for committing by the 
   <a href="/windows/desktop/api/vsprov/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots">CommitSnapshots</a> method call 
   that will follow. While the provider is processing this method, the applications have been frozen, so the time 
   spent in this method  should be minimized.

## -parameters

### -param SnapshotSetId [in]

The <b>VSS_ID</b> that identifies the shadow copy set.

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