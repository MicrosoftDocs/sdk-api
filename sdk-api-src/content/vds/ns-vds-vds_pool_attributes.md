---
UID: NS:vds._VDS_POOL_ATTRIBUTES
title: VDS_POOL_ATTRIBUTES (vds.h)
description: The VDS_POOL_ATTRIBUTES structure (vds.h) defines the attributes of a storage pool. 
helpviewer_keywords: ["*PVDS_POOL_ATTRIBUTES","PVDS_POOL_ATTRIBUTES","PVDS_POOL_ATTRIBUTES structure pointer","VDS_POOL_ATTRIBUTES","VDS_POOL_ATTRIBUTES structure","VDS_POOL_ATTRIB_ACCS_BDW_WT_HINT","VDS_POOL_ATTRIB_ACCS_DIR_HINT","VDS_POOL_ATTRIB_ACCS_LTNCY_HINT","VDS_POOL_ATTRIB_ACCS_RNDM_HINT","VDS_POOL_ATTRIB_ACCS_SIZE_HINT","VDS_POOL_ATTRIB_ALLOW_SPINDOWN","VDS_POOL_ATTRIB_BUSTYPE","VDS_POOL_ATTRIB_CUSTOM_ATTRIB","VDS_POOL_ATTRIB_DATA_AVL_HINT","VDS_POOL_ATTRIB_DATA_RDNCY_DEF","VDS_POOL_ATTRIB_DATA_RDNCY_MAX","VDS_POOL_ATTRIB_DATA_RDNCY_MIN","VDS_POOL_ATTRIB_NO_SINGLE_POF","VDS_POOL_ATTRIB_NUM_CLMNS","VDS_POOL_ATTRIB_NUM_CLMNS_DEF","VDS_POOL_ATTRIB_NUM_CLMNS_MAX","VDS_POOL_ATTRIB_NUM_CLMNS_MIN","VDS_POOL_ATTRIB_PKG_RDNCY_DEF","VDS_POOL_ATTRIB_PKG_RDNCY_MAX","VDS_POOL_ATTRIB_PKG_RDNCY_MIN","VDS_POOL_ATTRIB_RAIDTYPE","VDS_POOL_ATTRIB_STOR_COST_HINT","VDS_POOL_ATTRIB_STOR_EFFCY_HINT","VDS_POOL_ATTRIB_STRIPE_SIZE","VDS_POOL_ATTRIB_STRIPE_SIZE_DEF","VDS_POOL_ATTRIB_STRIPE_SIZE_MAX","VDS_POOL_ATTRIB_STRIPE_SIZE_MIN","VDS_POOL_ATTRIB_THIN_PROVISION","base.vds_pool_attributes","vds/PVDS_POOL_ATTRIBUTES","vds/VDS_POOL_ATTRIBUTES","vdshwprv/PVDS_POOL_ATTRIBUTES","vdshwprv/VDS_POOL_ATTRIBUTES"]
old-location: base\vds_pool_attributes.htm
tech.root: base
ms.assetid: 3dfbd3d9-ec2e-44ac-9d0f-7aa6c530db18
ms.date: 08/05/2022
ms.keywords: '*PVDS_POOL_ATTRIBUTES, PVDS_POOL_ATTRIBUTES, PVDS_POOL_ATTRIBUTES structure pointer, VDS_POOL_ATTRIBUTES, VDS_POOL_ATTRIBUTES structure, VDS_POOL_ATTRIB_ACCS_BDW_WT_HINT, VDS_POOL_ATTRIB_ACCS_DIR_HINT, VDS_POOL_ATTRIB_ACCS_LTNCY_HINT, VDS_POOL_ATTRIB_ACCS_RNDM_HINT, VDS_POOL_ATTRIB_ACCS_SIZE_HINT, VDS_POOL_ATTRIB_ALLOW_SPINDOWN, VDS_POOL_ATTRIB_BUSTYPE, VDS_POOL_ATTRIB_CUSTOM_ATTRIB, VDS_POOL_ATTRIB_DATA_AVL_HINT, VDS_POOL_ATTRIB_DATA_RDNCY_DEF, VDS_POOL_ATTRIB_DATA_RDNCY_MAX, VDS_POOL_ATTRIB_DATA_RDNCY_MIN, VDS_POOL_ATTRIB_NO_SINGLE_POF, VDS_POOL_ATTRIB_NUM_CLMNS, VDS_POOL_ATTRIB_NUM_CLMNS_DEF, VDS_POOL_ATTRIB_NUM_CLMNS_MAX, VDS_POOL_ATTRIB_NUM_CLMNS_MIN, VDS_POOL_ATTRIB_PKG_RDNCY_DEF, VDS_POOL_ATTRIB_PKG_RDNCY_MAX, VDS_POOL_ATTRIB_PKG_RDNCY_MIN, VDS_POOL_ATTRIB_RAIDTYPE, VDS_POOL_ATTRIB_STOR_COST_HINT, VDS_POOL_ATTRIB_STOR_EFFCY_HINT, VDS_POOL_ATTRIB_STRIPE_SIZE, VDS_POOL_ATTRIB_STRIPE_SIZE_DEF, VDS_POOL_ATTRIB_STRIPE_SIZE_MAX, VDS_POOL_ATTRIB_STRIPE_SIZE_MIN, VDS_POOL_ATTRIB_THIN_PROVISION, base.vds_pool_attributes, vds/PVDS_POOL_ATTRIBUTES, vds/VDS_POOL_ATTRIBUTES, vdshwprv/PVDS_POOL_ATTRIBUTES, vdshwprv/VDS_POOL_ATTRIBUTES'
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
req.typenames: VDS_POOL_ATTRIBUTES, *PVDS_POOL_ATTRIBUTES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_POOL_ATTRIBUTES
 - vds/_VDS_POOL_ATTRIBUTES
 - PVDS_POOL_ATTRIBUTES
 - vds/PVDS_POOL_ATTRIBUTES
 - VDS_POOL_ATTRIBUTES
 - vds/VDS_POOL_ATTRIBUTES
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
 - VDS_POOL_ATTRIBUTES
---

# VDS_POOL_ATTRIBUTES structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the attributes of a <a href="/windows/desktop/VDS/storage-pool-object">storage pool</a>.

## -struct-fields

### -field ullAttributeMask

A mask that specifies the attributes in the structure that are defined by this storage pool. 


The list of valid attribute flags is as follows. Each flag corresponds to a member in the <b>VDS_POOL_ATTRIBUTES</b> structure. Unused bits are reserved.



<table>
<tr>
<th>Value</th>
<th>Attribute defined by the storage pool</th>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_RAIDTYPE"></a><a id="vds_pool_attrib_raidtype"></a><dl>
<dt><b>VDS_POOL_ATTRIB_RAIDTYPE</b></dt>
<dt>0x1L</dt>
</dl>
</td>
<td width="60%">
<b>raidType</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_BUSTYPE"></a><a id="vds_pool_attrib_bustype"></a><dl>
<dt><b>VDS_POOL_ATTRIB_BUSTYPE</b></dt>
<dt>0x2L</dt>
</dl>
</td>
<td width="60%">
<b>busType</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_ALLOW_SPINDOWN"></a><a id="vds_pool_attrib_allow_spindown"></a><dl>
<dt><b>VDS_POOL_ATTRIB_ALLOW_SPINDOWN</b></dt>
<dt>0x4L</dt>
</dl>
</td>
<td width="60%">
<b>bSpinDown</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_THIN_PROVISION"></a><a id="vds_pool_attrib_thin_provision"></a><dl>
<dt><b>VDS_POOL_ATTRIB_THIN_PROVISION</b></dt>
<dt>0x8L</dt>
</dl>
</td>
<td width="60%">
<b>bIsThinProvisioned</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_NO_SINGLE_POF"></a><a id="vds_pool_attrib_no_single_pof"></a><dl>
<dt><b>VDS_POOL_ATTRIB_NO_SINGLE_POF</b></dt>
<dt>0x10L</dt>
</dl>
</td>
<td width="60%">
<b>bNoSinglePointOfFailure</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_DATA_RDNCY_MAX"></a><a id="vds_pool_attrib_data_rdncy_max"></a><dl>
<dt><b>VDS_POOL_ATTRIB_DATA_RDNCY_MAX</b></dt>
<dt>0x20L</dt>
</dl>
</td>
<td width="60%">
<b>ulDataRedundancyMax</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_DATA_RDNCY_MIN"></a><a id="vds_pool_attrib_data_rdncy_min"></a><dl>
<dt><b>VDS_POOL_ATTRIB_DATA_RDNCY_MIN</b></dt>
<dt>0x40L</dt>
</dl>
</td>
<td width="60%">
<b>ulDataRedundancyMin</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_DATA_RDNCY_DEF"></a><a id="vds_pool_attrib_data_rdncy_def"></a><dl>
<dt><b>VDS_POOL_ATTRIB_DATA_RDNCY_DEF</b></dt>
<dt>0x80L</dt>
</dl>
</td>
<td width="60%">
<b>ulDataRedundancyDefault</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_PKG_RDNCY_MAX"></a><a id="vds_pool_attrib_pkg_rdncy_max"></a><dl>
<dt><b>VDS_POOL_ATTRIB_PKG_RDNCY_MAX</b></dt>
<dt>0x100L</dt>
</dl>
</td>
<td width="60%">
<b>ulPackageRedundancyDefault</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_PKG_RDNCY_MIN"></a><a id="vds_pool_attrib_pkg_rdncy_min"></a><dl>
<dt><b>VDS_POOL_ATTRIB_PKG_RDNCY_MIN</b></dt>
<dt>0x200L</dt>
</dl>
</td>
<td width="60%">
<b>ulPackageRedundancyMin</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_PKG_RDNCY_DEF"></a><a id="vds_pool_attrib_pkg_rdncy_def"></a><dl>
<dt><b>VDS_POOL_ATTRIB_PKG_RDNCY_DEF</b></dt>
<dt>0x400L</dt>
</dl>
</td>
<td width="60%">
<b>ulPackageRedundancyDefault</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_STRIPE_SIZE"></a><a id="vds_pool_attrib_stripe_size"></a><dl>
<dt><b>VDS_POOL_ATTRIB_STRIPE_SIZE</b></dt>
<dt>0x800L</dt>
</dl>
</td>
<td width="60%">
<b>ulStripeSize</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_STRIPE_SIZE_MAX"></a><a id="vds_pool_attrib_stripe_size_max"></a><dl>
<dt><b>VDS_POOL_ATTRIB_STRIPE_SIZE_MAX</b></dt>
<dt>0x1000L</dt>
</dl>
</td>
<td width="60%">
<b>ulStripeSizeMax</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_STRIPE_SIZE_MIN"></a><a id="vds_pool_attrib_stripe_size_min"></a><dl>
<dt><b>VDS_POOL_ATTRIB_STRIPE_SIZE_MIN</b></dt>
<dt>0x2000L</dt>
</dl>
</td>
<td width="60%">
<b>ulStripeSizeMin</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_STRIPE_SIZE_DEF"></a><a id="vds_pool_attrib_stripe_size_def"></a><dl>
<dt><b>VDS_POOL_ATTRIB_STRIPE_SIZE_DEF</b></dt>
<dt>0x4000L</dt>
</dl>
</td>
<td width="60%">
<b>ulDefaultStripeSize</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_NUM_CLMNS"></a><a id="vds_pool_attrib_num_clmns"></a><dl>
<dt><b>VDS_POOL_ATTRIB_NUM_CLMNS</b></dt>
<dt>0x8000L</dt>
</dl>
</td>
<td width="60%">
<b>ulNumberOfColumns</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_NUM_CLMNS_MAX"></a><a id="vds_pool_attrib_num_clmns_max"></a><dl>
<dt><b>VDS_POOL_ATTRIB_NUM_CLMNS_MAX</b></dt>
<dt>0x10000L</dt>
</dl>
</td>
<td width="60%">
<b>ulNumberOfColumnsMax</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_NUM_CLMNS_MIN"></a><a id="vds_pool_attrib_num_clmns_min"></a><dl>
<dt><b>VDS_POOL_ATTRIB_NUM_CLMNS_MIN</b></dt>
<dt>0x20000L</dt>
</dl>
</td>
<td width="60%">
<b>ulNumberOfColumnsMin</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_NUM_CLMNS_DEF"></a><a id="vds_pool_attrib_num_clmns_def"></a><dl>
<dt><b>VDS_POOL_ATTRIB_NUM_CLMNS_DEF</b></dt>
<dt>0x40000L</dt>
</dl>
</td>
<td width="60%">
<b>ulDefaultNumberofColumns</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_DATA_AVL_HINT"></a><a id="vds_pool_attrib_data_avl_hint"></a><dl>
<dt><b>VDS_POOL_ATTRIB_DATA_AVL_HINT</b></dt>
<dt>0x80000L</dt>
</dl>
</td>
<td width="60%">
<b>ulDataAvailabilityHint</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_ACCS_RNDM_HINT"></a><a id="vds_pool_attrib_accs_rndm_hint"></a><dl>
<dt><b>VDS_POOL_ATTRIB_ACCS_RNDM_HINT</b></dt>
<dt>0x100000L</dt>
</dl>
</td>
<td width="60%">
<b>ulAccessRandomnessHint</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_ACCS_DIR_HINT"></a><a id="vds_pool_attrib_accs_dir_hint"></a><dl>
<dt><b>VDS_POOL_ATTRIB_ACCS_DIR_HINT</b></dt>
<dt>0x200000L</dt>
</dl>
</td>
<td width="60%">
<b>ulAccessDirectionHint</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_ACCS_SIZE_HINT"></a><a id="vds_pool_attrib_accs_size_hint"></a><dl>
<dt><b>VDS_POOL_ATTRIB_ACCS_SIZE_HINT</b></dt>
<dt>0x400000L</dt>
</dl>
</td>
<td width="60%">
<b>ulAccessSizeHint</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_ACCS_LTNCY_HINT"></a><a id="vds_pool_attrib_accs_ltncy_hint"></a><dl>
<dt><b>VDS_POOL_ATTRIB_ACCS_LTNCY_HINT</b></dt>
<dt>0x800000L</dt>
</dl>
</td>
<td width="60%">
<b>ulAccessLatencyHint</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_ACCS_BDW_WT_HINT"></a><a id="vds_pool_attrib_accs_bdw_wt_hint"></a><dl>
<dt><b>VDS_POOL_ATTRIB_ACCS_BDW_WT_HINT</b></dt>
<dt>0x1000000L</dt>
</dl>
</td>
<td width="60%">
<b>ulAccessBandwidthWeightHint</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_STOR_COST_HINT"></a><a id="vds_pool_attrib_stor_cost_hint"></a><dl>
<dt><b>VDS_POOL_ATTRIB_STOR_COST_HINT</b></dt>
<dt>0x2000000L</dt>
</dl>
</td>
<td width="60%">
<b>ulStorageCostHint</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_STOR_EFFCY_HINT"></a><a id="vds_pool_attrib_stor_effcy_hint"></a><dl>
<dt><b>VDS_POOL_ATTRIB_STOR_EFFCY_HINT</b></dt>
<dt>0x4000000L</dt>
</dl>
</td>
<td width="60%">
<b>ulStorageEfficiencyHint</b>

</td>
</tr>
<tr>
<td width="40%"><a id="VDS_POOL_ATTRIB_CUSTOM_ATTRIB"></a><a id="vds_pool_attrib_custom_attrib"></a><dl>
<dt><b>VDS_POOL_ATTRIB_CUSTOM_ATTRIB</b></dt>
<dt>0x8000000L</dt>
</dl>
</td>
<td width="60%">
<b>pPoolCustomAttributes</b>

</td>
</tr>
</table>

### -field raidType

A  <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_raid_type">VDS_RAID_TYPE</a> enumeration value that specifies the RAID type of the storage pool. If the storage pool does not have a specific RAID type, set this member to <b>VDS_RT_UNKNOWN</b> and  clear the <b>VDS_POOL_ATTRIB_RAIDTYPE</b> attribute flag in the <b>ullAttributeMask</b> member.

### -field busType

A <a href="/windows/desktop/api/vdslun/ne-vdslun-vds_storage_bus_type">VDS_STORAGE_BUS_TYPE</a> enumeration value that specifies the bus type of the drives in the storage pool.

### -field pwszIntendedUsage

A string that specifies the usage of the storage pool. Typically, this may indicate the application that is using the storage pool (for example,  "SQL" or "Exchange") or the business function that is using the storage pool (for example, "Finance" or "Human Resources").

### -field bSpinDown

<b>TRUE</b> if the drives in the storage pool spin down automatically to reduce power usage, or <b>FALSE</b> otherwise.

### -field bIsThinProvisioned

<b>TRUE</b> if the storage pool is thin provisioned, or <b>FALSE</b> otherwise. If the pool is thin provisioned, the number of bytes in the consumed space of the pool could be less than the number of bytes in the provisioned space of the pool. (The number of bytes in the provisioned space is stored in the <b>ullProvisionedSpace</b> member of this structure. The number of bytes in the consumed space is stored in the <b>ullTotalConsumedSpace</b> member of the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_storage_pool_prop">VDS_STORAGE_POOL_PROP</a> structure.) When a hardware provider sets this member to <b>TRUE</b>, it must also set the <b>type</b> member of the <b>VDS_STORAGE_POOL_PROP</b> structure to <b>VDS_SPT_CONCRETE</b>.

### -field ullProvisionedSpace

If the pool is thin provisioned, this member specifies the space, in bytes, that is provisioned for the pool. The value of this member must be greater than or equal to the value of the <b>ullTotalConsumedSpace</b> member of the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_storage_pool_prop">VDS_STORAGE_POOL_PROP</a> structure.

### -field bNoSinglePointOfFailure

<b>TRUE</b> if there is no single point of failure in the pool, or <b>FALSE</b> otherwise.

### -field ulDataRedundancyMax

The maximum number of complete copies of the data that can be maintained in this storage pool.

### -field ulDataRedundancyMin

The minimum number of complete copies of the data that can be maintained in this storage pool.

### -field ulDataRedundancyDefault

The default number of complete copies of the data that are maintained in this storage pool.

### -field ulPackageRedundancyMax

The maximum number of drives that can be used in the storage pool to ensure package redundancy. Package redundancy indicates the number of drives that can fail in the storage pool without resulting in a data loss.

### -field ulPackageRedundancyMin

The minimum number of drives that can be used in the storage pool to ensure package redundancy. Package redundancy indicates the number of drives that can fail in the storage pool without resulting in a data loss.

### -field ulPackageRedundancyDefault

The default number of drives that are used in the storage pool to ensure package redundancy. Package redundancy indicates the number of drives that can fail in the storage pool without resulting in a data loss.

### -field ulStripeSize

The mirror or parity stripe size, in bytes, of the storage pool if the pool is striped (with or without parity).

### -field ulStripeSizeMax

The maximum stripe size, in bytes, that is supported by the storage pool.

### -field ulStripeSizeMin

The minimum stripe size, in bytes, that is supported by the storage pool.

### -field ulDefaultStripeSize

The default stripe size, in bytes, that is supported by the storage pool.

### -field ulNumberOfColumns

The number of columns of the storage pool if the pool is striped (with or without parity).

### -field ulNumberOfColumnsMax

The maximum number of columns supported by the storage pool.

### -field ulNumberOfColumnsMin

The minimum number of columns supported by the storage pool.

### -field ulDefaultNumberofColumns

The default number of columns supported by the storage pool.

### -field ulDataAvailabilityHint

A hint from the client that indicates the importance placed on data availability. Values range from 0 (Not Important) to 10 (Very Important).

### -field ulAccessRandomnessHint

A hint from the client that indicates the randomness of data access. Values range from 0 (Entirely Sequential) to 10 (Entirely Random).

### -field ulAccessDirectionHint

A hint from the client that indicates the direction of data access. Values range from 0 (Entirely Read) to 10 (Entirely Write).

### -field ulAccessSizeHint

A hint from the client that indicates the optimal access size in megabytes.

### -field ulAccessLatencyHint

A hint from the client that indicates the importance of access latency to the client. Values range from 0 (Not Important) to 10 (Very Important).

### -field ulAccessBandwidthWeightHint

A hint from the client that indicates the importance of high bandwidth. Values range from 0 (Not Important) to 10 (Very Important).

### -field ulStorageCostHint

A hint from the client that indicates the importance of storage cost to the client. Values range from 0 (Not Important) to 10 (Very Important). If the storage cost is very important to the client, a value of 10 indicates that the client would prefer to provision the pool using lower cost storage.

### -field ulStorageEfficiencyHint

A hint from the client that indicates the importance of storage efficiency to the client. Values range from 0 (Not Important) to 10 (Very Important).

### -field ulNumOfCustomAttributes

The number of custom attributes defined for the storage pool.

### -field pPoolCustomAttributes

An array of <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_pool_custom_attributes">VDS_POOL_CUSTOM_ATTRIBUTES</a> structures. Each structure contains a custom attribute that is defined for the storage pool.

### -field bReserved1

This member is reserved for future use. Do not use.

### -field bReserved2

This member is reserved for future use. Do not use.

### -field ulReserved1

This member is reserved for future use. Do not use.

### -field ulReserved2

This member is reserved for future use. Do not use.

### -field ullReserved1

This member is reserved for future use. Do not use.

### -field ullReserved2

This member is reserved for future use. Do not use.

## -remarks

If an attribute is set for a storage pool, that attribute setting must apply to all drive extents that make up the pool.

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdshwproviderstoragepools-querystoragepools">IVdsHwProviderStoragePools::QueryStoragePools</a>



<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsstoragepool-getattributes">IVdsStoragePool::GetAttributes</a>
