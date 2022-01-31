---
UID: NE:vds._VDS_STORAGE_POOL_TYPE
title: VDS_STORAGE_POOL_TYPE (vds.h)
description: Defines the set of storage pool types.
helpviewer_keywords: ["VDS_SPT_CONCRETE","VDS_SPT_PRIMORDIAL","VDS_SPT_UNKNOWN","VDS_STORAGE_POOL_TYPE","VDS_STORAGE_POOL_TYPE enumeration","base.vds_storage_pool_type","vds/VDS_SPT_CONCRETE","vds/VDS_SPT_PRIMORDIAL","vds/VDS_SPT_UNKNOWN","vds/VDS_STORAGE_POOL_TYPE","vdshwprv/VDS_SPT_CONCRETE","vdshwprv/VDS_SPT_PRIMORDIAL","vdshwprv/VDS_SPT_UNKNOWN","vdshwprv/VDS_STORAGE_POOL_TYPE"]
old-location: base\vds_storage_pool_type.htm
tech.root: base
ms.assetid: 813d3452-46ad-4f7a-ab53-e3f6577b00ba
ms.date: 12/05/2018
ms.keywords: VDS_SPT_CONCRETE, VDS_SPT_PRIMORDIAL, VDS_SPT_UNKNOWN, VDS_STORAGE_POOL_TYPE, VDS_STORAGE_POOL_TYPE enumeration, base.vds_storage_pool_type, vds/VDS_SPT_CONCRETE, vds/VDS_SPT_PRIMORDIAL, vds/VDS_SPT_UNKNOWN, vds/VDS_STORAGE_POOL_TYPE, vdshwprv/VDS_SPT_CONCRETE, vdshwprv/VDS_SPT_PRIMORDIAL, vdshwprv/VDS_SPT_UNKNOWN, vdshwprv/VDS_STORAGE_POOL_TYPE
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
req.typenames: VDS_STORAGE_POOL_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_STORAGE_POOL_TYPE
 - vds/_VDS_STORAGE_POOL_TYPE
 - VDS_STORAGE_POOL_TYPE
 - vds/VDS_STORAGE_POOL_TYPE
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
 - VDS_STORAGE_POOL_TYPE
---

# VDS_STORAGE_POOL_TYPE enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of <a href="/windows/desktop/VDS/storage-pool-object">storage pool</a> types. These values are used in the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_storage_pool_prop">type</a> member of the <b>VDS_STORAGE_POOL_PROP</b> structure.

## -enum-fields

### -field VDS_SPT_UNKNOWN:0

The storage pool type is unknown.

### -field VDS_SPT_PRIMORDIAL:0x1

The storage pool type is primordial.

### -field VDS_SPT_CONCRETE:0x2

The storage pool type is concrete (non-primordial).

## -remarks

The terms <i>primordial storage pool</i> and <i>concrete storage pool</i> are defined in section 5.1.3 of the "Part 3: Block Devices" portion of the <a href="https://www.snia.org/tech_activities/standards/curr_standards/smi/">SMI-S v1.5 specification</a>, which can be downloaded from the <a href="https://www.snia.org/">SNIA website</a>.

A storage area network (SAN) can contain one primordial pool. You can create multiple concrete pools within the primordial pool. The attributes in the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_pool_attributes">VDS_POOL_ATTRIBUTES</a> structure do not apply to a primordial pool, because it contains all physically available storage on the SAN. For example, suppose you have ten 10-GB SAN drives, five of which are in a concrete pool. In the Disk Management utility, the primordial pool has ten disk drives and a size of 100 GB, because it has a total of 100 GB of storage space available. The concrete pool has only 50 GB of storage space available. But if it is thin-provisioned, the size that the Disk Management utility reports for the concrete pool might be much larger than 50 GB.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_STORAGE_POOL_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_STORAGE_POOL_TYPE</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_storage_pool_prop">VDS_STORAGE_POOL_PROP</a>
