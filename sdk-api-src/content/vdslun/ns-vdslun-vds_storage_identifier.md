---
UID: NS:vdslun._VDS_STORAGE_IDENTIFIER
title: VDS_STORAGE_IDENTIFIER (vdslun.h)
description: Defines a storage device using a particular code set and type.
helpviewer_keywords: ["VDS_STORAGE_IDENTIFIER","VDS_STORAGE_IDENTIFIER structure [VDS]","base.vds_storage_identifier","vdslun/_VDS_STORAGE_IDENTIFIER"]
old-location: base\vds_storage_identifier.htm
tech.root: base
ms.assetid: 8cc8b6d9-e189-44af-9f2b-2222b2eb0749
ms.date: 12/05/2018
ms.keywords: VDS_STORAGE_IDENTIFIER, VDS_STORAGE_IDENTIFIER structure [VDS], base.vds_storage_identifier, vdslun/_VDS_STORAGE_IDENTIFIER
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
req.typenames: VDS_STORAGE_IDENTIFIER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_STORAGE_IDENTIFIER
 - vdslun/_VDS_STORAGE_IDENTIFIER
 - VDS_STORAGE_IDENTIFIER
 - vdslun/VDS_STORAGE_IDENTIFIER
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
 - VDS_STORAGE_IDENTIFIER
---

# VDS_STORAGE_IDENTIFIER structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines a 
   storage device using a particular code set and type.

## -struct-fields

### -field m_CodeSet

The encoding type of <b>m_rgbIdentifier</b> enumerated by 
      <a href="/windows/desktop/api/vdslun/ne-vdslun-vds_storage_identifier_code_set">VDS_STORAGE_IDENTIFIER_CODE_SET</a>.

### -field m_Type

The type of <b>m_rgbIdentifier</b> enumerated by 
      <a href="/windows/desktop/api/vdslun/ne-vdslun-vds_storage_identifier_type">VDS_STORAGE_IDENTIFIER_TYPE</a>.

### -field m_cbIdentifier

The size of the <b>m_rgbIdentifier</b> array, in bytes.

### -field m_rgbIdentifier

Pointer to the identifier data.

## -remarks

The <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_storage_device_id_descriptor">VDS_STORAGE_DEVICE_ID_DESCRIPTOR</a> 
    structure includes this structure as a member to specify a particular storage device identifier for a LUN.

## -see-also

<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vdslun/ns-vdslun-vds_storage_device_id_descriptor">VDS_STORAGE_DEVICE_ID_DESCRIPTOR</a>



<a href="/windows/desktop/api/vdslun/ne-vdslun-vds_storage_identifier_code_set">VDS_STORAGE_IDENTIFIER_CODE_SET</a>



<a href="/windows/desktop/api/vdslun/ne-vdslun-vds_storage_identifier_type">VDS_STORAGE_IDENTIFIER_TYPE</a>