---
UID: NF:vsprov.IVssProviderCreateSnapshotSet.PreFinalCommitSnapshots
title: IVssProviderCreateSnapshotSet::PreFinalCommitSnapshots (vsprov.h)
description: Enables providers to support auto-recover shadow copies.
helpviewer_keywords: ["IVssProviderCreateSnapshotSet interface [VSS]","PreFinalCommitSnapshots method","IVssProviderCreateSnapshotSet.PreFinalCommitSnapshots","IVssProviderCreateSnapshotSet::PreFinalCommitSnapshots","PreFinalCommitSnapshots","PreFinalCommitSnapshots method [VSS]","PreFinalCommitSnapshots method [VSS]","IVssProviderCreateSnapshotSet interface","base.ivssprovidercreatesnapshotset_prefinalcommitsnapshots","vsprov/IVssProviderCreateSnapshotSet::PreFinalCommitSnapshots"]
old-location: base\ivssprovidercreatesnapshotset_prefinalcommitsnapshots.htm
tech.root: base
ms.assetid: 6d6895b9-6e6c-4c4c-b7c9-a4eff771567a
ms.date: 12/05/2018
ms.keywords: IVssProviderCreateSnapshotSet interface [VSS],PreFinalCommitSnapshots method, IVssProviderCreateSnapshotSet.PreFinalCommitSnapshots, IVssProviderCreateSnapshotSet::PreFinalCommitSnapshots, PreFinalCommitSnapshots, PreFinalCommitSnapshots method [VSS], PreFinalCommitSnapshots method [VSS],IVssProviderCreateSnapshotSet interface, base.ivssprovidercreatesnapshotset_prefinalcommitsnapshots, vsprov/IVssProviderCreateSnapshotSet::PreFinalCommitSnapshots
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
 - IVssProviderCreateSnapshotSet::PreFinalCommitSnapshots
 - vsprov/IVssProviderCreateSnapshotSet::PreFinalCommitSnapshots
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
 - IVssProviderCreateSnapshotSet.PreFinalCommitSnapshots
---

# IVssProviderCreateSnapshotSet::PreFinalCommitSnapshots


## -description

The 
   <b>PreFinalCommitSnapshots</b> 
   method enables providers to support 
   <a href="/windows/desktop/VSS/vssgloss-a">auto-recover</a> shadow 
   copies. If the shadow copy has the <b>VSS_VOLSNAP_ATTR_AUTORECOVER</b> flag set in 
   the context, the volume can receive a large number of writes during the auto-recovery operation.

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

## -remarks

This method was added to enable binary compatibility when the 
    <a href="/windows/desktop/VSS/vssgloss-a">auto-recover</a> feature was introduced in 
    Windows Server 2003 with Service Pack 1 (SP1).

<div class="alert"><b>Note</b>  For Windows Server 2003, it is recommended that hardware providers implement this method using 
    the following example:</div>
<div> </div>

```cpp
HRESULT PreFinalCommitSnapshots(
VSS_ID     /* SnapshotSetId */
)
{
    return S_OK;
}

```

## -see-also

<a href="/windows/desktop/api/vsprov/nn-vsprov-ivssprovidercreatesnapshotset">IVssProviderCreateSnapshotSet</a>