---
UID: NS:vds._VDS_STORAGE_POOL_PROP
title: VDS_STORAGE_POOL_PROP (vds.h)
description: The VDS_STORAGE_POOL_PROP structure (vds.h) defines the properties of a storage pool object.
helpviewer_keywords: ["*PVDS_STORAGE_POOL_PROP","PVDS_STORAGE_POOL_PROP","PVDS_STORAGE_POOL_PROP structure pointer","VDS_H_DEGRADED","VDS_H_HEALTHY","VDS_H_UNKNOWN","VDS_STORAGE_POOL_PROP","VDS_STORAGE_POOL_PROP structure","base.vds_storage_pool_prop","vds/PVDS_STORAGE_POOL_PROP","vds/VDS_STORAGE_POOL_PROP","vdshwprv/PVDS_STORAGE_POOL_PROP","vdshwprv/VDS_STORAGE_POOL_PROP"]
old-location: base\vds_storage_pool_prop.htm
tech.root: base
ms.assetid: 2a82e872-2005-4b05-b67a-161b16c4f3aa
ms.date: 08/05/2022
ms.keywords: '*PVDS_STORAGE_POOL_PROP, PVDS_STORAGE_POOL_PROP, PVDS_STORAGE_POOL_PROP structure pointer, VDS_H_DEGRADED, VDS_H_HEALTHY, VDS_H_UNKNOWN, VDS_STORAGE_POOL_PROP, VDS_STORAGE_POOL_PROP structure, base.vds_storage_pool_prop, vds/PVDS_STORAGE_POOL_PROP, vds/VDS_STORAGE_POOL_PROP, vdshwprv/PVDS_STORAGE_POOL_PROP, vdshwprv/VDS_STORAGE_POOL_PROP'
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
req.typenames: VDS_STORAGE_POOL_PROP, *PVDS_STORAGE_POOL_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_STORAGE_POOL_PROP
 - vds/_VDS_STORAGE_POOL_PROP
 - PVDS_STORAGE_POOL_PROP
 - vds/PVDS_STORAGE_POOL_PROP
 - VDS_STORAGE_POOL_PROP
 - vds/VDS_STORAGE_POOL_PROP
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
 - VDS_STORAGE_POOL_PROP
---

# VDS_STORAGE_POOL_PROP structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the properties of a <a href="/windows/desktop/VDS/storage-pool-object">storage pool object</a>.

## -struct-fields

### -field id

A <a href="/windows/desktop/VDS/vds-data-types">VDS_OBJECT_ID</a> value that identifies the storage pool object.

### -field status

A <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_storage_pool_status">VDS_STORAGE_POOL_STATUS</a> enumeration value that specifies the status of the storage pool.

### -field health

A <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_health">VDS_HEALTH</a> enumeration value that specifies the health of the storage pool. The following are the valid values for this member.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b><b>VDS_H_DEGRADED</b> is not supported.



#### VDS_H_UNKNOWN (0)



#### VDS_H_HEALTHY (1)



#### VDS_H_DEGRADED (11)

### -field type

A <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_storage_pool_type">VDS_STORAGE_POOL_TYPE</a> enumeration value that specifies the type of the storage pool.

### -field pwszName

A string that specifies the name of the storage pool.

### -field pwszDescription

A string that contains a description of the storage pool.

### -field ullTotalConsumedSpace

The amount of physical storage backing  the storage pool, in bytes. The value of this member must be less than or equal to the value of the <b>ullProvisionedSpace</b> member of the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_pool_attributes">VDS_POOL_ATTRIBUTES</a> structure.

### -field ullTotalManagedSpace

The space, in bytes, in this storage pool that can be allocated to create child storage elements (LUNs or pools), including space that has already been allocated. Depending on the way the storage pool is configured, the value of this member can be much less than the value of the <b>ullTotalConsumedSpace</b> member. For example, if the storage pool is configured as a mirrored pool, the value of <b>ullTotalManagedSpace</b> is only half as large as the value of the <b>ullTotalConsumedSpace</b> member.

### -field ullRemainingFreeSpace

The maximum size that may be used to create new LUNs or child storage pools from this pool, or to expand existing LUNs or child storage pools. To calculate the amount of managed space that has already been allocated to existing LUNs or child storage pools, subtract the value of this member from the value of the <b>ullTotalManagedSpace</b> member.

## -remarks

The <a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsstoragepool-getproperties">IVdsStoragePool::GetProperties</a> returns this structure to report the properties of a <a href="/windows/desktop/VDS/storage-pool-object">storage pool object</a>.

The following examples show how the <b>ullTotalConsumedSpace</b>, <b>ullTotalManagedSpace</b>, and <b>ullRemainingFreeSpace</b> members work together.

<h3><a id="Example_1"></a><a id="example_1"></a><a id="EXAMPLE_1"></a>Example 1</h3>
Suppose you have 2 drives of 1 TB each. Suppose further that you do the following:<ol>
<li>Create a storage pool as a mirror pool.</li>
<li>Create a LUN whose size is 200 GB.</li>
</ol>


<b>ullTotalConsumedSpace</b> = 2 TB. This is the amount of storage pool space  that is backed by physical storage or physical disks. Creating LUNs from the pool does not change this number.

<b>ullTotalManagedSpace</b> = 1 TB. This is the maximum size of the LUN or storage pool that can be created from this pool. Only 1 TB is available, because the pool type is a mirror with only 2 plexes. <div class="alert"><b>Note</b>  If the pool type were RAID5, <b>ullTotalManagedSpace</b> would be (<i>N</i>-1)/<i>N</i> * <b>ullTotalConsumedSpace</b>, where <i>N</i> is the number of columns. For example, with 5 drives and 5 columns, <b>ullTotalManagedSpace</b> would be (5-1)/5 * <b>ullTotalConsumedSpace</b> or 1.6 TB.</div>
<div> </div>


<b>ullRemainingFreeSpace</b> = 800 GB (1 TB – 200 GB), because 200GB has already been allocated to a LUN.

(<b>ullTotalManagedSpace</b> -  <b>ullRemainingFreeSpace</b>) is the amount of managed space allocated to LUNs and pools created from this pool. In this example, <b>ullTotalManagedSpace</b> -  <b>ullRemainingFreeSpace</b> = 200 GB.

<h3><a id="Example_2"></a><a id="example_2"></a><a id="EXAMPLE_2"></a>Example 2</h3>
Suppose you have 2 drives of 1 TB each. Suppose further that you do the following:<ol>
<li>Create a storage pool as a mirror pool.</li>
<li>Create a thin-provisioned LUN whose size is 10 TB.</li>
</ol>


<b>ullProvisionedSpace</b> = 10 TB. This applies only to thin-provisioned pools. This is the total space provisioned for the pool. The total space consumed by the pool is less than or equal to the total space provisioned for the pool.

<b>ullTotalConsumedSpace</b> = 2 TB.

<b>ullTotalManagedSpace</b> = 1 TB.

<b>ullRemainingFreeSpace</b> = 1 TB minus the amount of  managed space currently backing the LUN.  <div class="alert"><b>Note</b>  Although the LUN's size is 10 TB, there may be as little as 10 GB of managed space backing the LUN, in which case there would be 20 GB of consumed space backing the mirrored LUN.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/vdshwprv/nf-vdshwprv-ivdsstoragepool-getproperties">IVdsStoragePool::GetProperties</a>
