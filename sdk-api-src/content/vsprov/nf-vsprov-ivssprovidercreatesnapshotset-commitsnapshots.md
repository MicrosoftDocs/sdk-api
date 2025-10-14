---
UID: NF:vsprov.IVssProviderCreateSnapshotSet.CommitSnapshots
title: IVssProviderCreateSnapshotSet::CommitSnapshots (vsprov.h)
description: Quickly commits all LUNs in this provider.
helpviewer_keywords: ["CommitSnapshots","CommitSnapshots method [VSS]","CommitSnapshots method [VSS]","IVssProviderCreateSnapshotSet interface","IVssProviderCreateSnapshotSet interface [VSS]","CommitSnapshots method","IVssProviderCreateSnapshotSet.CommitSnapshots","IVssProviderCreateSnapshotSet::CommitSnapshots","base.ivssprovidercreatesnapshotset_commitsnapshots","vsprov/IVssProviderCreateSnapshotSet::CommitSnapshots"]
old-location: base\ivssprovidercreatesnapshotset_commitsnapshots.htm
tech.root: base
ms.assetid: 60489142-125f-4deb-afa0-9dae63ea1d46
ms.date: 12/05/2018
ms.keywords: CommitSnapshots, CommitSnapshots method [VSS], CommitSnapshots method [VSS],IVssProviderCreateSnapshotSet interface, IVssProviderCreateSnapshotSet interface [VSS],CommitSnapshots method, IVssProviderCreateSnapshotSet.CommitSnapshots, IVssProviderCreateSnapshotSet::CommitSnapshots, base.ivssprovidercreatesnapshotset_commitsnapshots, vsprov/IVssProviderCreateSnapshotSet::CommitSnapshots
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
 - IVssProviderCreateSnapshotSet::CommitSnapshots
 - vsprov/IVssProviderCreateSnapshotSet::CommitSnapshots
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
 - IVssProviderCreateSnapshotSet.CommitSnapshots
---

# IVssProviderCreateSnapshotSet::CommitSnapshots


## -description

The <b>CommitSnapshots</b> 
   method quickly commits all LUNs in this provider.

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
An unexpected provider error occurred. The provider must log the details of this error in the application 
        event log.

</td>
</tr>
</table>
 

If any other value is returned, VSS will write an event to the event log and convert the error to 
      <b>VSS_E_UNEXPECTED_PROVIDER_ERROR</b>.

## -remarks

This method is called at the defined time at which the shadow copies should be taken. For each prepared LUN 
    in this shadow copy set, the provider will perform the work required to persist the point-in-time LUN contents. 
    While this method is executing, both applications and the I/O subsystem are largely quiescent. The provider must 
    minimize the amount of time spent in this method. As a general rule, this method should take less than one second 
    to complete. This method is called during the Flush and Hold window, and VSS Kernel Support will 
     cancel the Flush and Hold if the release is not received within 10 seconds, which would cause VSS to fail the 
     shadow copy creation process. If each provider takes more than  a second or two to complete this call, there is a 
     high probability that the entire shadow copy creation will fail.

Because the I/O system is quiescent, the provider must take care to not initiate any I/O as it could deadlock 
    the system - for example debug or tracing I/O by this method or any calls made from this method. Memory mapped 
    files and paging I/O will not be frozen at this time.

Note that the I/O system is quiescent only while this method is executing. Immediately after the last provider's <b>CommitSnapshots</b> method returns, the VSS service releases all pending writes on the source LUNs. If the provider performs any synchronization of the source and shadow copy LUNs, this synchronization must be completed before the provider's <b>CommitSnapshots</b> method returns;  it cannot be performed asynchronously.

## -see-also

<a href="/windows/desktop/api/vsprov/nn-vsprov-ivssprovidercreatesnapshotset">IVssProviderCreateSnapshotSet</a>