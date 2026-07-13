---
UID: NF:vsprov.IVssProviderCreateSnapshotSet.AbortSnapshots
title: IVssProviderCreateSnapshotSet::AbortSnapshots (vsprov.h)
description: Aborts prepared shadow copies in this provider.
helpviewer_keywords: ["AbortSnapshots","AbortSnapshots method [VSS]","AbortSnapshots method [VSS]","IVssProviderCreateSnapshotSet interface","IVssProviderCreateSnapshotSet interface [VSS]","AbortSnapshots method","IVssProviderCreateSnapshotSet.AbortSnapshots","IVssProviderCreateSnapshotSet::AbortSnapshots","base.ivssprovidercreatesnapshotset_abortsnapshots","vsprov/IVssProviderCreateSnapshotSet::AbortSnapshots"]
old-location: base\ivssprovidercreatesnapshotset_abortsnapshots.htm
tech.root: base
ms.assetid: 393fd5aa-9934-4918-8699-25c41d0dc982
ms.date: 12/05/2018
ms.keywords: AbortSnapshots, AbortSnapshots method [VSS], AbortSnapshots method [VSS],IVssProviderCreateSnapshotSet interface, IVssProviderCreateSnapshotSet interface [VSS],AbortSnapshots method, IVssProviderCreateSnapshotSet.AbortSnapshots, IVssProviderCreateSnapshotSet::AbortSnapshots, base.ivssprovidercreatesnapshotset_abortsnapshots, vsprov/IVssProviderCreateSnapshotSet::AbortSnapshots
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
 - IVssProviderCreateSnapshotSet::AbortSnapshots
 - vsprov/IVssProviderCreateSnapshotSet::AbortSnapshots
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
 - IVssProviderCreateSnapshotSet.AbortSnapshots
---

# IVssProviderCreateSnapshotSet::AbortSnapshots


## -description

The <b>AbortSnapshots</b> 
   method aborts prepared shadow copies in this provider. This includes all non-committed shadow 
   copies and pre-committed ones.

## -parameters

### -param SnapshotSetId [in]

The <b>VSS_ID</b> that identifies the shadow copy set.

## -returns

This method can return one of these values.

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
An unexpected provider error occurred. The provider must log a message in the application event log 
        providing the user with information on how to resolve the problem.

</td>
</tr>
</table>

## -remarks

VSS will only call 
    <b>AbortSnapshots</b> after the 
    requester has called 
    <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset">IVssBackupComponents::DoSnapshotSet</a>, 
    even if the shadow copy fails or is aborted before this point. This means that a provider will not receive an 
    <b>AbortSnapshots</b> call until 
    after <a href="/windows/desktop/api/vsprov/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots">EndPrepareSnapshots</a> 
    has been called. If a shadow copy is aborted or fails before this point, the provider is not given any indication 
    until a new shadow copy is started. For this reason, the provider must be prepared to handle an out-of-sequence 
    <a href="/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot">IVssHardwareSnapshotProvider::BeginPrepareSnapshot</a> 
    call at any point. This out-of-sequence call represents the start of a new shadow copy creation sequence and will 
    have a new shadow copy set ID.

## -see-also

<a href="/windows/desktop/api/vsprov/nn-vsprov-ivssprovidercreatesnapshotset">IVssProviderCreateSnapshotSet</a>