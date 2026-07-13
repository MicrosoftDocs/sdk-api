---
UID: NS:vdslun._VDS_STORAGE_DEVICE_ID_DESCRIPTOR
title: VDS_STORAGE_DEVICE_ID_DESCRIPTOR (vdslun.h)
description: Defines one or more storage identifiers for a storage device (typically an instance, as opposed to a class, of device).
helpviewer_keywords: ["VDS_STORAGE_DEVICE_ID_DESCRIPTOR","VDS_STORAGE_DEVICE_ID_DESCRIPTOR structure [VDS]","base.vds_storage_device_id_descriptor","vdslun/_VDS_STORAGE_DEVICE_ID_DESCRIPTOR"]
old-location: base\vds_storage_device_id_descriptor.htm
tech.root: base
ms.assetid: 88fe83cb-6d3c-40bd-a5ce-71771d2e7511
ms.date: 12/05/2018
ms.keywords: VDS_STORAGE_DEVICE_ID_DESCRIPTOR, VDS_STORAGE_DEVICE_ID_DESCRIPTOR structure [VDS], base.vds_storage_device_id_descriptor, vdslun/_VDS_STORAGE_DEVICE_ID_DESCRIPTOR
req.header: vdslun.h
req.include-header: Vds.h, VdsHwPrv.h for hardware providers
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
req.typenames: VDS_STORAGE_DEVICE_ID_DESCRIPTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_STORAGE_DEVICE_ID_DESCRIPTOR
 - vdslun/_VDS_STORAGE_DEVICE_ID_DESCRIPTOR
 - VDS_STORAGE_DEVICE_ID_DESCRIPTOR
 - vdslun/VDS_STORAGE_DEVICE_ID_DESCRIPTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - VdsLun.h
api_name:
 - VDS_STORAGE_DEVICE_ID_DESCRIPTOR
---

# VDS_STORAGE_DEVICE_ID_DESCRIPTOR structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines one or more storage identifiers for a storage device (typically an instance, as opposed to a 
   class, of device).

## -struct-fields

### -field m_version

The version of this structure.

### -field m_cIdentifiers

The number of identifiers specified in <b>m_rgIdentifiers</b>.

### -field m_rgIdentifiers

Pointer to <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_storage_identifier">VDS_STORAGE_IDENTIFIER</a> structure.

## -remarks

Storage devices can have multiple identifiers, and each of these identifiers can have a different code set and 
    type. The <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> structure includes 
    this structure as a member to specify the storage device identifiers of a LUN.

## -see-also

<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a>



<a href="/windows/desktop/api/vdslun/ns-vdslun-vds_storage_identifier">VDS_STORAGE_IDENTIFIER</a>