---
UID: NF:vsprov.IVssHardwareSnapshotProvider.GetTargetLuns
title: IVssHardwareSnapshotProvider::GetTargetLuns (vsprov.h)
description: Prompts the hardware provider to initialize the VDS_LUN_INFORMATION structures for the newly created shadow copy LUNs.
helpviewer_keywords: ["GetTargetLuns","GetTargetLuns method [VSS]","GetTargetLuns method [VSS]","IVssHardwareSnapshotProvider interface","IVssHardwareSnapshotProvider interface [VSS]","GetTargetLuns method","IVssHardwareSnapshotProvider.GetTargetLuns","IVssHardwareSnapshotProvider::GetTargetLuns","base.ivsshardwaresnapshotprovider_gettargetluns","vsprov/IVssHardwareSnapshotProvider::GetTargetLuns"]
old-location: base\ivsshardwaresnapshotprovider_gettargetluns.htm
tech.root: base
ms.assetid: 299020eb-0afd-41c8-9551-1275eff45fa1
ms.date: 12/05/2018
ms.keywords: GetTargetLuns, GetTargetLuns method [VSS], GetTargetLuns method [VSS],IVssHardwareSnapshotProvider interface, IVssHardwareSnapshotProvider interface [VSS],GetTargetLuns method, IVssHardwareSnapshotProvider.GetTargetLuns, IVssHardwareSnapshotProvider::GetTargetLuns, base.ivsshardwaresnapshotprovider_gettargetluns, vsprov/IVssHardwareSnapshotProvider::GetTargetLuns
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
 - IVssHardwareSnapshotProvider::GetTargetLuns
 - vsprov/IVssHardwareSnapshotProvider::GetTargetLuns
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
 - IVssHardwareSnapshotProvider.GetTargetLuns
---

# IVssHardwareSnapshotProvider::GetTargetLuns


## -description

The <b>GetTargetLuns</b> method prompts the hardware provider to initialize the <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> structures for the newly created shadow copy LUNs. The <b>GetTargetLuns</b> method 
    is called after 
    the <a href="/windows/desktop/api/vsprov/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots">IVssProviderCreateSnapshotSet::PostCommitSnapshots</a> method. 
    Identifying information for each newly created LUN is returned to VSS through 
    <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> structures.
<div class="alert"><b>Note</b>  Hardware providers are only supported on Windows Server operating systems.</div><div> </div>

## -parameters

### -param lLunCount [in]

Count of LUNs that contribute to the original volume.

### -param rgDeviceNames [in]

Pointer to an array of <i>lLunCount</i> pointers to strings. Each string contains 
      the name of an original LUN to be shadow copied.

### -param rgSourceLuns [in]

Pointer to an array of <i>lLunCount</i><a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> structures, one for each LUN 
      that contributes to the original volume.

### -param rgDestinationLuns [in, out]

Pointer to an array of <i>lLunCount</i><a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> structures, one for each new 
      shadow copy LUN created during shadow copy processing. There should be a one-to-one correspondence between the elements of 
      the <i>rgSourceLuns</i> and <i>rgDestinationLuns</i> arrays.

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

In the <i>rgDestinationLuns</i> parameter, VSS supplies an empty <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> 
    structure for each newly created shadow copy LUN. The shadow copy LUNs are not surfaced or visible to the system. 
    The provider should initialize the members of the 
    <b>VDS_LUN_INFORMATION</b> structure with the appropriate SCSI 
    Inquiry Data and Vital Product Data page  80 (device serial number) and page 83 (device identity) information. The 
    structure should contain correct member values such that the shadow copy LUNs can be located by Windows from the 
    original computer or any other computer connected to the SAN.

The members of the <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> structure correspond to the page 80 information, with the following exceptions:

<ul>
<li>The <b>m_version</b> member must be set to <b>VER_VDS_LUN_INFORMATION</b>.</li>
<li>The <b>m_BusType</b> member is ignored in comparisons during import. This value depends on the PnP storage stack on the corresponding disk device. Usually this is <b>VDSBusTypeScsi</b>.</li>
<li>The <b>m_diskSignature</b> member is ignored in comparisons during import. The provider must set this member to GUID_NULL.</li>
</ul>
The members of the <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_storage_device_id_descriptor">VDS_STORAGE_DEVICE_ID_DESCRIPTOR</a> 
      structure (in the <b>m_deviceIdDescriptor</b> member of the <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> 
    structure) correspond to the page 83 information. In this structure, each <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_storage_identifier">VDS_STORAGE_IDENTIFIER</a> 
      structure corresponds to the STORAGE_IDENTIFIER structure for a device identifier (that is, a storage identifier with an association type of zero). For more information about the STORAGE_IDENTIFIER structure, see the Windows Driver Kit (WDK) documentation.

The <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> structures returned here 
    must be the same as the structures provided in 
    the <a href="/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotprovider-fillinluninfo">IVssHardwareSnapshotProvider::FillInLunInfo</a> method during import so 
    that VSS can use this information to identify the newly arriving shadow copy LUNs at import. These same structures 
    will be passed to the provider in the 
    <a href="/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotprovider-locateluns">IVssHardwareSnapshotProvider::LocateLuns</a> method.

## -see-also

<a href="/windows/desktop/api/vsprov/nn-vsprov-ivsshardwaresnapshotprovider">IVssHardwareSnapshotProvider</a>



<a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a>