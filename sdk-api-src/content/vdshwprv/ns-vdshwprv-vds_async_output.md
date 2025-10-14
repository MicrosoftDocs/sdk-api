---
UID: NS:vdshwprv._VDS_ASYNC_OUTPUT
title: VDS_ASYNC_OUTPUT (vdshwprv.h)
description: The VDS_ASYNC_OUTPUT structure (vdshwprv.h) defines the output of an async object. Output elements vary depending on the operation type.
helpviewer_keywords: ["VDS_ASYNCOUT_BREAKVOLUMEPLEX","VDS_ASYNCOUT_CREATELUN","VDS_ASYNCOUT_CREATEPARTITION","VDS_ASYNCOUT_CREATEPORTALGROUP","VDS_ASYNCOUT_CREATETARGET","VDS_ASYNCOUT_CREATEVOLUME","VDS_ASYNCOUT_CREATE_VDISK","VDS_ASYNC_OUTPUT","VDS_ASYNC_OUTPUT structure [VDS]","base.vds_async_output","vds/_VDS_ASYNC_OUTPUT","vdshwprv/_VDS_ASYNC_OUTPUT"]
old-location: base\vds_async_output.htm
tech.root: base
ms.assetid: 21771c6a-eca9-47f3-b6fc-383bca1e11bf
ms.date: 08/08/2022
ms.keywords: VDS_ASYNCOUT_BREAKVOLUMEPLEX, VDS_ASYNCOUT_CREATELUN, VDS_ASYNCOUT_CREATEPARTITION, VDS_ASYNCOUT_CREATEPORTALGROUP, VDS_ASYNCOUT_CREATETARGET, VDS_ASYNCOUT_CREATEVOLUME, VDS_ASYNCOUT_CREATE_VDISK, VDS_ASYNC_OUTPUT, VDS_ASYNC_OUTPUT structure [VDS], base.vds_async_output, vds/_VDS_ASYNC_OUTPUT, vdshwprv/_VDS_ASYNC_OUTPUT
req.header: vdshwprv.h
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
req.typenames: VDS_ASYNC_OUTPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_ASYNC_OUTPUT
 - vdshwprv/_VDS_ASYNC_OUTPUT
 - VDS_ASYNC_OUTPUT
 - vdshwprv/VDS_ASYNC_OUTPUT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
 - VdsHwPrv.h
api_name:
 - VDS_ASYNC_OUTPUT
---

# VDS_ASYNC_OUTPUT structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the 
   output of an async object. Output elements vary depending on the operation type.

## -struct-fields

### -field type

Discriminant for the union enumerated by 
      <a href="/windows/desktop/api/vds/ne-vds-vds_async_output_type">VDS_ASYNC_OUTPUT_TYPE</a>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VDS_ASYNCOUT_CREATEPARTITION"></a><a id="vds_asyncout_createpartition"></a><dl>
<dt><b>VDS_ASYNCOUT_CREATEPARTITION</b></dt>
<dt>10</dt>
</dl>
</td>
<td width="60%">
See the following description of the <b>cp</b> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_ASYNCOUT_CREATEVOLUME"></a><a id="vds_asyncout_createvolume"></a><dl>
<dt><b>VDS_ASYNCOUT_CREATEVOLUME</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
See the following description of the <b>cv</b> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_ASYNCOUT_BREAKVOLUMEPLEX"></a><a id="vds_asyncout_breakvolumeplex"></a><dl>
<dt><b>VDS_ASYNCOUT_BREAKVOLUMEPLEX</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
See the following description of the <b>bvp</b> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_ASYNCOUT_CREATELUN"></a><a id="vds_asyncout_createlun"></a><dl>
<dt><b>VDS_ASYNCOUT_CREATELUN</b></dt>
<dt>50</dt>
</dl>
</td>
<td width="60%">
See the following description of the <b>cl</b> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_ASYNCOUT_CREATETARGET"></a><a id="vds_asyncout_createtarget"></a><dl>
<dt><b>VDS_ASYNCOUT_CREATETARGET</b></dt>
<dt>62</dt>
</dl>
</td>
<td width="60%">
See the following description of the <b>ct</b> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_ASYNCOUT_CREATEPORTALGROUP"></a><a id="vds_asyncout_createportalgroup"></a><dl>
<dt><b>VDS_ASYNCOUT_CREATEPORTALGROUP</b></dt>
<dt>63</dt>
</dl>
</td>
<td width="60%">
See the following description of the <b>cpg</b> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_ASYNCOUT_CREATE_VDISK"></a><a id="vds_asyncout_create_vdisk"></a><dl>
<dt><b>VDS_ASYNCOUT_CREATE_VDISK</b></dt>
<dt>200</dt>
</dl>
</td>
<td width="60%">
See the following description of the <b>cvd</b> structure.

</td>
</tr>
</table>

### -field cp

Structure used for the 
       <a href="/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-createpartition">IVdsAdvancedDisk::CreatePartition</a> or
       <a href="/windows/desktop/api/vds/nf-vds-ivdscreatepartitionex-createpartitionex">IVdsCreatePartitionEx::CreatePartitionEx</a> 
       method.

### -field cp.ullOffset

Actual offset of the created partition. This may not be the same as the 
        <i>ullOffset</i> parameter passed to the 
        <a href="/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-createpartition">IVdsAdvancedDisk::CreatePartition</a> or 
        <a href="/windows/desktop/api/vds/nf-vds-ivdscreatepartitionex-createpartitionex">IVdsCreatePartitionEx::CreatePartitionEx</a> 
        method.

### -field cp.volumeId

The ID of the <a href="/windows/desktop/VDS/volume-object">volume object</a> associated with the 
        created partition.

### -field cv

Structure used for the 
       <a href="/windows/desktop/api/vds/nf-vds-ivdspack-createvolume">IVdsPack::CreateVolume</a> method.

### -field cv.pVolumeUnk

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> for the volume object. For more information, see 
        <a href="/windows/desktop/VDS/volume-object">Volume Object</a>.

### -field bvp

Structure used for the <a href="/windows/desktop/api/vds/nf-vds-ivdsvolume-breakplex">IVdsVolume::BreakPlex</a> 
       method.

### -field bvp.pVolumeUnk

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> for the volume object. For more information, see 
        <a href="/windows/desktop/VDS/volume-object">Volume Object</a>.

### -field sv

Structure used for the <a href="/windows/desktop/api/vds/nf-vds-ivdsvolume-shrink">IVdsVolume::Shrink</a> 
       method.

### -field sv.ullReclaimedBytes

The number of bytes that were reclaimed by the shrink operation.

<b>Windows Server 2003:  </b> This member is not supported until Windows Server 2003 R2.

### -field cl

Structure used for the 
       <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystem-createlun">IVdsSubSystem::CreateLun</a> method.

### -field cl.pLunUnk

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> for the LUN object. For more information, see 
        <a href="/windows/desktop/VDS/lun-object">LUN Object</a>.

### -field ct

Structure used for the 
       <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdssubsystemiscsi-createtarget">IVdsSubSystemIscsi::CreateTarget</a> method.

### -field ct.pTargetUnk

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> for the target object. 
        For more information, see the <a href="/windows/desktop/VDS/target-object">Target Object</a>.

### -field cpg

Structure used for the 
       <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsiscsitarget-createportalgroup">IVdsIscsiTarget::CreatePortalGroup</a> method.

### -field cpg.pPortalGroupUnk

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> for the portal group object. 
        For more information, see the <a href="/windows/desktop/VDS/portal-group-object">Portal Group Object</a>.

### -field cvd

Structure used for the 
       <a href="/windows/desktop/api/vds/nf-vds-ivdsvdprovider-createvdisk">IVdsVdProvider::CreateVDisk</a> method.

### -field cvd.pVDiskUnk

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> for the virtual disk object.

## -remarks

The <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-wait">IVdsAsync::Wait</a> method returns this structure 
    and adds a reference to any contained object produced by each method. 
    Callers must release the reference to the contained object.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsasync-wait">IVdsAsync::Wait</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_async_output_type">VDS_ASYNC_OUTPUT_TYPE</a>
