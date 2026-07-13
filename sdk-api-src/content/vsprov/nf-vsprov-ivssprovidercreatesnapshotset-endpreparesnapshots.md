---
UID: NF:vsprov.IVssProviderCreateSnapshotSet.EndPrepareSnapshots
title: IVssProviderCreateSnapshotSet::EndPrepareSnapshots (vsprov.h)
description: Is called once for the complete shadow copy set, after the last IVssHardwareSnapshotProvider::BeginPrepareSnapshot call.
helpviewer_keywords: ["EndPrepareSnapshots","EndPrepareSnapshots method [VSS]","EndPrepareSnapshots method [VSS]","IVssProviderCreateSnapshotSet interface","IVssProviderCreateSnapshotSet interface [VSS]","EndPrepareSnapshots method","IVssProviderCreateSnapshotSet.EndPrepareSnapshots","IVssProviderCreateSnapshotSet::EndPrepareSnapshots","base.ivssprovidercreatesnapshotset_endpreparesnapshots","vsprov/IVssProviderCreateSnapshotSet::EndPrepareSnapshots"]
old-location: base\ivssprovidercreatesnapshotset_endpreparesnapshots.htm
tech.root: base
ms.assetid: 230666c7-e7e4-4e75-a84d-1786e8cbbb6c
ms.date: 12/05/2018
ms.keywords: EndPrepareSnapshots, EndPrepareSnapshots method [VSS], EndPrepareSnapshots method [VSS],IVssProviderCreateSnapshotSet interface, IVssProviderCreateSnapshotSet interface [VSS],EndPrepareSnapshots method, IVssProviderCreateSnapshotSet.EndPrepareSnapshots, IVssProviderCreateSnapshotSet::EndPrepareSnapshots, base.ivssprovidercreatesnapshotset_endpreparesnapshots, vsprov/IVssProviderCreateSnapshotSet::EndPrepareSnapshots
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
 - IVssProviderCreateSnapshotSet::EndPrepareSnapshots
 - vsprov/IVssProviderCreateSnapshotSet::EndPrepareSnapshots
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
 - IVssProviderCreateSnapshotSet.EndPrepareSnapshots
---

# IVssProviderCreateSnapshotSet::EndPrepareSnapshots


## -description

The <b>EndPrepareSnapshots</b> 
   method is called once for the complete shadow copy set, after the last 
   <a href="/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot">IVssHardwareSnapshotProvider::BeginPrepareSnapshot</a> 
   call. This method is intended as a point where the provider can wait for any shadow copy preparation 
   work to complete. Because 
   <b>EndPrepareSnapshots</b> may 
   take a long time to complete, a provider should be prepared to accept an 
   <a href="/windows/desktop/api/vsprov/nf-vsprov-ivssprovidercreatesnapshotset-abortsnapshots">AbortSnapshots</a> method call 
   at any time and immediately end the preparation work.

## -parameters

### -param SnapshotSetId [in]

The <b>VSS_ID</b> of the shadow copy set.

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
<dt><b>VSS_E_INSUFFICIENT_STORAGE</b></dt>
<dt>0x8004231FL</dt>
</dl>
</td>
<td width="60%">
There is not enough disk storage to create a shadow copy. Insufficient disk space can also generate 
        <b>VSS_E_PROVIDER_VETO</b> or <b>VSS_E_OBJECT_NOT_FOUND</b> error 
        return values.

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

<a href="/windows/desktop/api/vsprov/nf-vsprov-ivssprovidercreatesnapshotset-abortsnapshots">AbortSnapshots</a>



<a href="/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot">IVssHardwareSnapshotProvider::BeginPrepareSnapshot</a>



<a href="/windows/desktop/api/vsprov/nn-vsprov-ivssprovidercreatesnapshotset">IVssProviderCreateSnapshotSet</a>