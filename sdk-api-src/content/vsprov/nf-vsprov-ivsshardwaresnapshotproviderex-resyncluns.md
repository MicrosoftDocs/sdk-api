---
UID: NF:vsprov.IVssHardwareSnapshotProviderEx.ResyncLuns
title: IVssHardwareSnapshotProviderEx::ResyncLuns (vsprov.h)
description: The VSS service calls this method to notify hardware providers that a LUN resynchronization is needed.
helpviewer_keywords: ["IVssHardwareSnapshotProviderEx interface","ResyncLuns method","IVssHardwareSnapshotProviderEx.ResyncLuns","IVssHardwareSnapshotProviderEx::ResyncLuns","ResyncLuns","ResyncLuns method","ResyncLuns method","IVssHardwareSnapshotProviderEx interface","base.ivsshardwaresnapshotproviderex_resyncluns","vsprov/IVssHardwareSnapshotProviderEx::ResyncLuns"]
old-location: base\ivsshardwaresnapshotproviderex_resyncluns.htm
tech.root: base
ms.assetid: 27322ba0-e318-45d4-824e-8c81a18abd49
ms.date: 12/05/2018
ms.keywords: IVssHardwareSnapshotProviderEx interface,ResyncLuns method, IVssHardwareSnapshotProviderEx.ResyncLuns, IVssHardwareSnapshotProviderEx::ResyncLuns, ResyncLuns, ResyncLuns method, ResyncLuns method,IVssHardwareSnapshotProviderEx interface, base.ivsshardwaresnapshotproviderex_resyncluns, vsprov/IVssHardwareSnapshotProviderEx::ResyncLuns
req.header: vsprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssHardwareSnapshotProviderEx::ResyncLuns
 - vsprov/IVssHardwareSnapshotProviderEx::ResyncLuns
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
 - IVssHardwareSnapshotProviderEx.ResyncLuns
---

# IVssHardwareSnapshotProviderEx::ResyncLuns


## -description

The VSS service calls this method to notify hardware providers that a LUN resynchronization is needed.<div class="alert"><b>Note</b>  Hardware providers are only supported on Windows Server operating systems.</div>
<div> </div>

## -parameters

### -param pSourceLuns [in]

A pointer to an array of <i>dwCount</i> <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> structures,  one for each LUN that contributes to the shadow copy volume.

### -param pTargetLuns [in]

A pointer to an array of <i>dwCount</i> <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> structures,  one for each LUN that contributes to the destination volume where the contents of the shadow copy volume are to be copied.

### -param dwCount [in]

The number of elements in the <i>pSourceLuns</i> array. This is also the number of elements in the <i>pTargetLuns</i> array.

### -param ppAsync [out]

A pointer to a location that will receive an <a href="/windows/desktop/api/vss/nn-vss-ivssasync">IVssAsync</a> interface pointer that can be used to retrieve the status of the resynchronization operation. When the operation is complete, the caller must release the interface pointer by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method.

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
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
<dt>0x80042306L</dt>
</dl>
</td>
<td width="60%">
An unexpected provider error occurred. If this error code is returned, the error must be described in an entry in 
        the application event log, giving the user information on how to resolve the problem.

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
The provider cannot perform the operation because there is not enough disk space.

</td>
</tr>
</table>

## -remarks

The destination LUNs can be the LUNs that contribute to the original production volume from which the shadow copy was created, or they can be new or existing LUNs that are used to replace an original volume  that is removed from production.

The provider must perform the resynchronization by copying data at the LUN array level, not at the host level.  This means that the provider cannot implement LUN resynchronization by simply copying the contents of the source LUN to the destination LUN. The I/O that is required to perform the LUN resynchronization must be performed in the hardware, through the disk devices of the resynchronized LUNs, and not through the host computer. This I/O should be completely transparent to the host computer.

When the resynchronization is complete, the LUNs are fully functional and are available for I/O operations.

The underlying disk hardware must support unique page 83 device identifiers.

If the destination LUN is larger than the source LUN, the provider must resize the destination LUN if necessary to ensure that it matches the source LUN after resynchronization.

This method cannot be called in WinPE, and it cannot be called in Safe mode. Before calling this method, the caller must use the <a href="/windows/desktop/api/vsbackup/nf-vsbackup-ivssbackupcomponents-initializeforrestore">IVssBackupComponents::InitializeForRestore</a> method to prepare for the resynchronization.

## -see-also

<a href="/windows/desktop/api/vsprov/nn-vsprov-ivsshardwaresnapshotproviderex">IVssHardwareSnapshotProviderEx</a>