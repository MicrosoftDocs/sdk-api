---
UID: NF:vsprov.IVssHardwareSnapshotProvider.AreLunsSupported
title: IVssHardwareSnapshotProvider::AreLunsSupported (vsprov.h)
description: Determines whether the hardware provider supports shadow copy creation for all LUNs that contribute to the volume.
helpviewer_keywords: ["AreLunsSupported","AreLunsSupported method [VSS]","AreLunsSupported method [VSS]","IVssHardwareSnapshotProvider interface","IVssHardwareSnapshotProvider interface [VSS]","AreLunsSupported method","IVssHardwareSnapshotProvider.AreLunsSupported","IVssHardwareSnapshotProvider::AreLunsSupported","base.ivsshardwaresnapshotprovider_arelunssupported","vsprov/IVssHardwareSnapshotProvider::AreLunsSupported"]
old-location: base\ivsshardwaresnapshotprovider_arelunssupported.htm
tech.root: base
ms.assetid: f3615770-63a1-49eb-a3b9-b4d349fc33df
ms.date: 12/05/2018
ms.keywords: AreLunsSupported, AreLunsSupported method [VSS], AreLunsSupported method [VSS],IVssHardwareSnapshotProvider interface, IVssHardwareSnapshotProvider interface [VSS],AreLunsSupported method, IVssHardwareSnapshotProvider.AreLunsSupported, IVssHardwareSnapshotProvider::AreLunsSupported, base.ivsshardwaresnapshotprovider_arelunssupported, vsprov/IVssHardwareSnapshotProvider::AreLunsSupported
req.header: vsprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
 - IVssHardwareSnapshotProvider::AreLunsSupported
 - vsprov/IVssHardwareSnapshotProvider::AreLunsSupported
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
 - IVssHardwareSnapshotProvider.AreLunsSupported
---

# IVssHardwareSnapshotProvider::AreLunsSupported


## -description

The <b>AreLunsSupported</b> method determines whether the hardware provider supports shadow copy creation for all LUNs that contribute to the volume. VSS calls the <b>AreLunsSupported</b> 
    method for each volume that is added to the shadow copy set.  Before 
    calling this method, VSS determines the LUNs that contribute to the volume.

For a specific volume, each LUN can contribute only once. A specific LUN may contribute to multiple volumes.
<div class="alert"><b>Note</b>  Hardware providers are only supported on Windows Server operating systems.</div><div> </div>

## -parameters

### -param lLunCount [in]

Count of LUNs contributing to this shadow copy volume.

### -param lContext [in]

Shadow copy context for the current shadow copy set as enumerated by 
      a bitmask of flags from the <a href="/windows/desktop/api/vss/ne-vss-vss_volume_snapshot_attributes">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a> enumeration. If the <b>VSS_VOLSNAP_ATTR_TRANSPORTABLE</b> flag is set, the shadow copy set is transportable.

### -param rgwszDevices [in]

List of devices corresponding to the LUNs to be shadow copied.

### -param pLunInformation [in, out]

Array of <i>lLunCount</i><a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> structures, one for each LUN 
      contributing to this shadow copy volume.

### -param pbIsSupported [out]

Pointer to a <b>BOOL</b> value. If all devices are supported for shadow copy, the 
      provider should store a <b>TRUE</b> value at the location pointed to by 
      <i>pbIsSupported</i>.

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
<dt><b>VSS_E_PROVIDER_VETO</b></dt>
<dt>0x80042306L</dt>
</dl>
</td>
<td width="60%">
An unexpected provider error occurred. The provider must report an event in the application event log 
        providing the user with information on how to resolve the problem.

</td>
</tr>
</table>

## -remarks

If the hardware subsystem supports the SCSI Inquiry Data and Vital Product Data 
    page  80 (device serial number) and page 83 (device identity) guidelines, the provider should not need to modify the structures in the <i>pLunInformation</i> array.

In any case, the <b>AreLunsSupported</b> method should not modify the value of the <b>m_rgInterconnects</b> member of any <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> structure in the <i>pLunInformation</i> array.

If the provider supports hardware shadow copy creation for all of the LUNs in the <i>pLunInformation</i> array, it should return <b>TRUE</b> in the <b>BOOL</b> value that the <i>pbIsSupported</i> parameter points to. If the provider does not support hardware shadow copies for one or more LUNs, it must set this <b>BOOL</b> value to <b>FALSE</b>. 

The provider must never agree to create shadow copies if it cannot, even if the problem is only temporary. If a transient condition, such as low resources, makes it impossible for the provider to create a shadow copy using one or more LUNs   when <b>AreLunsSupported</b> is called, the provider must set the <b>BOOL</b> value to <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/api/vsprov/nn-vsprov-ivsshardwaresnapshotprovider">IVssHardwareSnapshotProvider</a>



<a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a>



<a href="/windows/desktop/api/vss/ne-vss-vss_volume_snapshot_attributes">_VSS_VOLUME_SNAPSHOT_ATTRIBUTES</a>