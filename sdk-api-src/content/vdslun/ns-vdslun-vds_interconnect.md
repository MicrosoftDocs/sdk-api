---
UID: NS:vdslun._VDS_INTERCONNECT
title: VDS_INTERCONNECT (vdslun.h)
description: Defines the address data of a physical interconnect.
helpviewer_keywords: ["VDS_INTERCONNECT","VDS_INTERCONNECT structure [VDS]","base.vds_interconnect","vdslun/_VDS_INTERCONNECT"]
old-location: base\vds_interconnect.htm
tech.root: base
ms.assetid: fc9f532b-a37f-4338-95db-6ec988131211
ms.date: 12/05/2018
ms.keywords: VDS_INTERCONNECT, VDS_INTERCONNECT structure [VDS], base.vds_interconnect, vdslun/_VDS_INTERCONNECT
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
req.typenames: VDS_INTERCONNECT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_INTERCONNECT
 - vdslun/_VDS_INTERCONNECT
 - VDS_INTERCONNECT
 - vdslun/VDS_INTERCONNECT
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
 - VDS_INTERCONNECT
---

# VDS_INTERCONNECT structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the address 
   data of a physical interconnect.

## -struct-fields

### -field m_addressType

The interconnect address type enumerated by 
      <a href="/windows/desktop/api/vdslun/ne-vdslun-vds_interconnect_address_type">VDS_INTERCONNECT_ADDRESS_TYPE</a>.

### -field m_cbPort

The size of the interconnect address data for the LUN port (<b>m_pbPort</b>), in bytes.

### -field m_pbPort

Pointer to the interconnect address data for the LUN port.

### -field m_cbAddress

The size of the interconnect address data for the LUN (<b>m_pbAddress</b>), in bytes.

### -field m_pbAddress

Pointer to the interconnect address data for the LUN.

## -remarks

The <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a> structure includes this 
    structure as a member to specify an interconnect by which a LUN can be accessed.

## -see-also

<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdslun/ne-vdslun-vds_interconnect_address_type">VDS_INTERCONNECT_ADDRESS_TYPE</a>



<a href="/windows/desktop/api/vdslun/ns-vdslun-vds_lun_information">VDS_LUN_INFORMATION</a>