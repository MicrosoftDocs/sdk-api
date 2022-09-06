---
UID: NE:vds._VDS_STORAGE_POOL_STATUS
title: VDS_STORAGE_POOL_STATUS (vds.h)
description: Defines the set of object status values for a storage pool.
helpviewer_keywords: ["VDS_SPS_NOT_READY","VDS_SPS_OFFLINE","VDS_SPS_ONLINE","VDS_SPS_UNKNOWN","VDS_STORAGE_POOL_STATUS","VDS_STORAGE_POOL_STATUS enumeration","base.vds_storage_pool_status","vds/VDS_SPS_NOT_READY","vds/VDS_SPS_OFFLINE","vds/VDS_SPS_ONLINE","vds/VDS_SPS_UNKNOWN","vds/VDS_STORAGE_POOL_STATUS","vdshwprv/VDS_SPS_NOT_READY","vdshwprv/VDS_SPS_OFFLINE","vdshwprv/VDS_SPS_ONLINE","vdshwprv/VDS_SPS_UNKNOWN","vdshwprv/VDS_STORAGE_POOL_STATUS"]
old-location: base\vds_storage_pool_status.htm
tech.root: base
ms.assetid: b2af30c8-116c-4e51-bffc-0dee9a4bd04e
ms.date: 12/05/2018
ms.keywords: VDS_SPS_NOT_READY, VDS_SPS_OFFLINE, VDS_SPS_ONLINE, VDS_SPS_UNKNOWN, VDS_STORAGE_POOL_STATUS, VDS_STORAGE_POOL_STATUS enumeration, base.vds_storage_pool_status, vds/VDS_SPS_NOT_READY, vds/VDS_SPS_OFFLINE, vds/VDS_SPS_ONLINE, vds/VDS_SPS_UNKNOWN, vds/VDS_STORAGE_POOL_STATUS, vdshwprv/VDS_SPS_NOT_READY, vdshwprv/VDS_SPS_OFFLINE, vdshwprv/VDS_SPS_ONLINE, vdshwprv/VDS_SPS_UNKNOWN, vdshwprv/VDS_STORAGE_POOL_STATUS
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
req.typenames: VDS_STORAGE_POOL_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_STORAGE_POOL_STATUS
 - vds/_VDS_STORAGE_POOL_STATUS
 - VDS_STORAGE_POOL_STATUS
 - vds/VDS_STORAGE_POOL_STATUS
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
 - VDS_STORAGE_POOL_STATUS
---

# VDS_STORAGE_POOL_STATUS enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of object status values for a <a href="/windows/desktop/VDS/storage-pool-object">storage pool</a>.

## -enum-fields

### -field VDS_SPS_UNKNOWN:0

The provider failed to get the storage pool properties or could not access the storage pool.

### -field VDS_SPS_ONLINE:1

The storage pool is available.

### -field VDS_SPS_NOT_READY:2

The storage pool is busy.

### -field VDS_SPS_OFFLINE:4

The storage pool is not available.

## -remarks

The <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_storage_pool_prop">VDS_STORAGE_POOL_PROP</a> structure uses a <b>VDS_STORAGE_POOL_STATUS</b> value in the <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_storage_pool_prop">status</a> member to indicate the current status of the storage pool.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_STORAGE_POOL_STATUS</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_STORAGE_POOL_STATUS</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_storage_pool_prop">VDS_STORAGE_POOL_PROP</a>
