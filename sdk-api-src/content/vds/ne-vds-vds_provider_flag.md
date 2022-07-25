---
UID: NE:vds._VDS_PROVIDER_FLAG
title: VDS_PROVIDER_FLAG (vds.h)
description: Defines the set of valid flags for a provider object.
helpviewer_keywords: ["VDS_PF_DYNAMIC","VDS_PF_INTERNAL_HARDWARE_PROVIDER","VDS_PF_ONE_DISK_ONLY_PER_PACK","VDS_PF_ONE_PACK_ONLINE_ONLY","VDS_PF_SUPPORT_DYNAMIC","VDS_PF_SUPPORT_DYNAMIC_1394","VDS_PF_SUPPORT_FAULT_TOLERANT","VDS_PF_SUPPORT_MIRROR","VDS_PF_SUPPORT_RAID5","VDS_PF_VOLUME_SPACE_MUST_BE_CONTIGUOUS","VDS_PROVIDER_FLAG","VDS_PROVIDER_FLAG enumeration [VDS]","base.vds_provider_flag","vds/VDS_PF_DYNAMIC","vds/VDS_PF_INTERNAL_HARDWARE_PROVIDER","vds/VDS_PF_ONE_DISK_ONLY_PER_PACK","vds/VDS_PF_ONE_PACK_ONLINE_ONLY","vds/VDS_PF_SUPPORT_DYNAMIC","vds/VDS_PF_SUPPORT_DYNAMIC_1394","vds/VDS_PF_SUPPORT_FAULT_TOLERANT","vds/VDS_PF_SUPPORT_MIRROR","vds/VDS_PF_SUPPORT_RAID5","vds/VDS_PF_VOLUME_SPACE_MUST_BE_CONTIGUOUS","vds/VDS_PROVIDER_FLAG","vdshwprv/VDS_PF_DYNAMIC","vdshwprv/VDS_PF_INTERNAL_HARDWARE_PROVIDER","vdshwprv/VDS_PF_ONE_DISK_ONLY_PER_PACK","vdshwprv/VDS_PF_ONE_PACK_ONLINE_ONLY","vdshwprv/VDS_PF_SUPPORT_DYNAMIC","vdshwprv/VDS_PF_SUPPORT_DYNAMIC_1394","vdshwprv/VDS_PF_SUPPORT_FAULT_TOLERANT","vdshwprv/VDS_PF_SUPPORT_MIRROR","vdshwprv/VDS_PF_SUPPORT_RAID5","vdshwprv/VDS_PF_VOLUME_SPACE_MUST_BE_CONTIGUOUS","vdshwprv/VDS_PROVIDER_FLAG"]
old-location: base\vds_provider_flag.htm
tech.root: base
ms.assetid: 610e11a8-6670-4e76-baa6-58dd78f7611b
ms.date: 12/05/2018
ms.keywords: VDS_PF_DYNAMIC, VDS_PF_INTERNAL_HARDWARE_PROVIDER, VDS_PF_ONE_DISK_ONLY_PER_PACK, VDS_PF_ONE_PACK_ONLINE_ONLY, VDS_PF_SUPPORT_DYNAMIC, VDS_PF_SUPPORT_DYNAMIC_1394, VDS_PF_SUPPORT_FAULT_TOLERANT, VDS_PF_SUPPORT_MIRROR, VDS_PF_SUPPORT_RAID5, VDS_PF_VOLUME_SPACE_MUST_BE_CONTIGUOUS, VDS_PROVIDER_FLAG, VDS_PROVIDER_FLAG enumeration [VDS], base.vds_provider_flag, vds/VDS_PF_DYNAMIC, vds/VDS_PF_INTERNAL_HARDWARE_PROVIDER, vds/VDS_PF_ONE_DISK_ONLY_PER_PACK, vds/VDS_PF_ONE_PACK_ONLINE_ONLY, vds/VDS_PF_SUPPORT_DYNAMIC, vds/VDS_PF_SUPPORT_DYNAMIC_1394, vds/VDS_PF_SUPPORT_FAULT_TOLERANT, vds/VDS_PF_SUPPORT_MIRROR, vds/VDS_PF_SUPPORT_RAID5, vds/VDS_PF_VOLUME_SPACE_MUST_BE_CONTIGUOUS, vds/VDS_PROVIDER_FLAG, vdshwprv/VDS_PF_DYNAMIC, vdshwprv/VDS_PF_INTERNAL_HARDWARE_PROVIDER, vdshwprv/VDS_PF_ONE_DISK_ONLY_PER_PACK, vdshwprv/VDS_PF_ONE_PACK_ONLINE_ONLY, vdshwprv/VDS_PF_SUPPORT_DYNAMIC, vdshwprv/VDS_PF_SUPPORT_DYNAMIC_1394, vdshwprv/VDS_PF_SUPPORT_FAULT_TOLERANT, vdshwprv/VDS_PF_SUPPORT_MIRROR, vdshwprv/VDS_PF_SUPPORT_RAID5, vdshwprv/VDS_PF_VOLUME_SPACE_MUST_BE_CONTIGUOUS, vdshwprv/VDS_PROVIDER_FLAG
req.header: vds.h
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
req.typenames: VDS_PROVIDER_FLAG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_PROVIDER_FLAG
 - vds/_VDS_PROVIDER_FLAG
 - VDS_PROVIDER_FLAG
 - vds/VDS_PROVIDER_FLAG
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
 - VDS_PROVIDER_FLAG
---

# VDS_PROVIDER_FLAG enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set 
   of valid flags for a provider object.

## -enum-fields

### -field VDS_PF_DYNAMIC:0x1

The provider is a dynamic  provider. If this flag is set for the provider of a disk, the disk is dynamic.

### -field VDS_PF_INTERNAL_HARDWARE_PROVIDER:0x2

The operating system supplies this hardware provider to manage an internal hardware controller.

### -field VDS_PF_ONE_DISK_ONLY_PER_PACK:0x4

The provider supports single-disk packs only. Typically, the basic provider sets this flag to 
      simulate a pack with one disk.

### -field VDS_PF_ONE_PACK_ONLINE_ONLY:0x8

The provider is a dynamic provider that supports online status for only one pack at a time. 
     

<b>Windows Server 2003:  </b>Only applies to this release.

### -field VDS_PF_VOLUME_SPACE_MUST_BE_CONTIGUOUS:0x10

All volumes managed by this provider must have contiguous space. This flag applies to basic 
      providers only.

### -field VDS_PF_SUPPORT_DYNAMIC:0x80000000

If this flag is set, VDS sets the <b>VDS_SVF_SUPPORT_DYNAMIC</b> flag in the <a href="/windows/desktop/api/vds/ns-vds-vds_service_prop">VDS_SERVICE_PROP</a> structure.

### -field VDS_PF_SUPPORT_FAULT_TOLERANT:0x40000000

If this flag is set, VDS sets the <b>VDS_SVF_SUPPORT_FAULT_TOLERANT</b> 
      flag in the <a href="/windows/desktop/api/vds/ns-vds-vds_service_prop">VDS_SERVICE_PROP</a> structure.

### -field VDS_PF_SUPPORT_DYNAMIC_1394:0x20000000

If this flag is set, VDS sets the <b>VDS_SVF_SUPPORT_DYNAMIC_1394</b> 
      flag in the <a href="/windows/desktop/api/vds/ns-vds-vds_service_prop">VDS_SERVICE_PROP</a> structure.

### -field VDS_PF_SUPPORT_MIRROR:0x20

If this flag is set, VDS sets the <b>VDS_SVF_SUPPORT_MIRROR</b> flag in the <a href="/windows/desktop/api/vds/ns-vds-vds_service_prop">VDS_SERVICE_PROP</a> structure.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Not supported.

### -field VDS_PF_SUPPORT_RAID5:0x40

If this flag is set, VDS sets the <b>VDS_SVF_SUPPORT_RAID5</b> flag in the <a href="/windows/desktop/api/vds/ns-vds-vds_service_prop">VDS_SERVICE_PROP</a> structure.

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>Not supported.

## -remarks

This enumeration provides the values for the <i>ulFlags</i> member of the 
    <a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_provider_prop">VDS_PROVIDER_PROP</a> structure.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_PROVIDER_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_PROVIDER_FLAG</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="/windows/desktop/api/vdshwprv/ns-vdshwprv-vds_provider_prop">VDS_PROVIDER_PROP</a>
