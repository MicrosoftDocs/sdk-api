---
UID: NF:vsprov.IVssHardwareSnapshotProvider.FillInLunInfo
title: IVssHardwareSnapshotProvider::FillInLunInfo (vsprov.h)
description: Prompts the hardware provider to indicate whether it supports the corresponding disk device and correct any omissions in the VDS_LUN_INFORMATION structure.
helpviewer_keywords: ["FillInLunInfo","FillInLunInfo method [VSS]","FillInLunInfo method [VSS]","IVssHardwareSnapshotProvider interface","IVssHardwareSnapshotProvider interface [VSS]","FillInLunInfo method","IVssHardwareSnapshotProvider.FillInLunInfo","IVssHardwareSnapshotProvider::FillInLunInfo","base.ivsshardwaresnapshotprovider_fillinluninfo","vsprov/IVssHardwareSnapshotProvider::FillInLunInfo"]
old-location: base\ivsshardwaresnapshotprovider_fillinluninfo.htm
tech.root: base
ms.assetid: 4e4e5942-5bc8-4b5e-a651-5bb354514994
ms.date: 12/05/2018
ms.keywords: FillInLunInfo, FillInLunInfo method [VSS], FillInLunInfo method [VSS],IVssHardwareSnapshotProvider interface, IVssHardwareSnapshotProvider interface [VSS],FillInLunInfo method, IVssHardwareSnapshotProvider.FillInLunInfo, IVssHardwareSnapshotProvider::FillInLunInfo, base.ivsshardwaresnapshotprovider_fillinluninfo, vsprov/IVssHardwareSnapshotProvider::FillInLunInfo
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
 - IVssHardwareSnapshotProvider::FillInLunInfo
 - vsprov/IVssHardwareSnapshotProvider::FillInLunInfo
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
 - IVssHardwareSnapshotProvider.FillInLunInfo
---

# IVssHardwareSnapshotProvider::FillInLunInfo


## -description

The 
   <b>FillInLunInfo</b> 
   method prompts the hardware provider to indicate whether it supports the corresponding disk device and correct any omissions in the <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> structure. VSS calls the 
   <b>FillInLunInfo</b> 
   method after the 
   <a href="/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotprovider-locateluns">IVssHardwareSnapshotProvider::LocateLuns</a> method or before 
   the <a href="/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotprovider-onlunempty">IVssHardwareSnapshotProvider::OnLunEmpty</a> method to obtain the 
   <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> structure associated with a 
   shadow copy LUN. VSS will compare the 
   <b>VDS_LUN_INFORMATION</b> structure received in 
   the <a href="/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotprovider-gettargetluns">IVssHardwareSnapshotProvider::GetTargetLuns</a> method to identify 
   shadow copy LUNs. If the structures do not match, the requester will receive 
   <b>VSS_S_SOME_SNAPSHOTS_NOT_IMPORTED</b>, which indicates a mismatch.
<div class="alert"><b>Note</b>  Hardware providers are only supported on Windows Server operating systems.</div><div> </div>

## -parameters

### -param wszDeviceName [in]

Device corresponding to the shadow copy LUN.

### -param pLunInfo [in, out]

The <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> structure for the 
      shadow copy LUN.

### -param pbIsSupported [out]

The provider must return <b>TRUE</b> in the location pointed to by the 
      <i>pbIsSupported</i> parameter if the device is supported.

## -returns

VSS  ignores this method's return value.

<b>Windows Server 2003:  </b>VSS does not ignore the return value, which can be one of the following values.

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
An unexpected provider error has occurred. The provider must report an event in the application event log 
        providing the user with information on how to resolve the problem.

</td>
</tr>
</table>

## -remarks

VSS calls the <b>FillInLunInfo</b> method for each <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> structure that the provider previously initialized in its <a href="/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotprovider-gettargetluns">GetTargetLuns</a> method. VSS also calls the <b>FillInLunInfo</b> method for each new disk device that arrives in the system during the import process. 

The provider can correct any omissions in the <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> structure received in the <i>pLunInfo</i>  parameter. However, the provider should not modify the value of the <b>m_rgInterconnects</b> member of this structure.

The members of the <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> structure correspond to the SCSI Inquiry Data and Vital Product Data page 80 (device serial number) information, with the following exceptions:

<ul>
<li>The <b>m_version</b> member must be set to <b>VER_VDS_LUN_INFORMATION</b>.</li>
<li>The <b>m_BusType</b> member is ignored in comparisons during import. This value depends on the PnP storage stack on the corresponding disk device. Usually this is <b>VDSBusTypeScsi</b>.</li>
<li>The <b>m_diskSignature</b> member is ignored in comparisons during import. The provider must set this member to GUID_NULL.</li>
</ul>
The members of the <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_storage_device_id_descriptor">VDS_STORAGE_DEVICE_ID_DESCRIPTOR</a> 
      structure (in the <b>m_deviceIdDescriptor</b> member of the <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> 
    structure) correspond to the page 83 information. In this structure, each <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_storage_identifier">VDS_STORAGE_IDENTIFIER</a> 
      structure corresponds to the STORAGE_IDENTIFIER structure for a device identifier (that is, a storage identifier with an association type of zero). For more information about the STORAGE_IDENTIFIER structure, see the Windows Driver Kit (WDK) documentation.

If the <b>FillInLunInfo</b> method is 
    called for a LUN that is unknown to the provider, the provider should not return an error. Instead, it 
    should return <b>FALSE</b>  in the <b>BOOL</b> value that the <i>pbIsSupported</i> parameter points to and 
    return success. If the provider recognizes the LUN, it should set the <b>BOOL</b> value to 
    <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported">AreLunsSupported</a>



<a href="/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotprovider-gettargetluns">GetTargetLuns</a>



<a href="/windows/desktop/api/vsprov/nn-vsprov-ivsshardwaresnapshotprovider">IVssHardwareSnapshotProvider</a>



<a href="/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotprovider-locateluns">LocateLuns</a>



<a href="/windows/desktop/api/vsprov/nf-vsprov-ivsshardwaresnapshotprovider-onlunempty">OnLunEmpty</a>



<a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a>



<a href="/windows/desktop/api/vdslun/ns-vdslun-vds_storage_identifier">VDS_STORAGE_IDENTIFIER</a>