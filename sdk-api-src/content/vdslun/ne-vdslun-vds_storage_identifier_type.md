---
UID: NE:vdslun._VDS_STORAGE_IDENTIFIER_TYPE
title: VDS_STORAGE_IDENTIFIER_TYPE (vdslun.h)
description: Defines the set of valid types for a storage identifier.
helpviewer_keywords: ["VDSStorageIdTypeEUI64","VDSStorageIdTypeFCPHName","VDSStorageIdTypePortRelative","VDSStorageIdTypeSCSINameString","VDSStorageIdTypeVendorId","VDSStorageIdTypeVendorSpecific","VDS_STORAGE_IDENTIFIER_TYPE","VDS_STORAGE_IDENTIFIER_TYPE enumeration [VDS]","base.vds_storage_identifier_type","vdslun/VDSStorageIdTypeEUI64","vdslun/VDSStorageIdTypeFCPHName","vdslun/VDSStorageIdTypePortRelative","vdslun/VDSStorageIdTypeSCSINameString","vdslun/VDSStorageIdTypeVendorId","vdslun/VDSStorageIdTypeVendorSpecific","vdslun/VDS_STORAGE_IDENTIFIER_TYPE"]
old-location: base\vds_storage_identifier_type.htm
tech.root: base
ms.assetid: 396ca6c1-fae3-4584-97c9-2c4dfbc170d5
ms.date: 12/05/2018
ms.keywords: VDSStorageIdTypeEUI64, VDSStorageIdTypeFCPHName, VDSStorageIdTypePortRelative, VDSStorageIdTypeSCSINameString, VDSStorageIdTypeVendorId, VDSStorageIdTypeVendorSpecific, VDS_STORAGE_IDENTIFIER_TYPE, VDS_STORAGE_IDENTIFIER_TYPE enumeration [VDS], base.vds_storage_identifier_type, vdslun/VDSStorageIdTypeEUI64, vdslun/VDSStorageIdTypeFCPHName, vdslun/VDSStorageIdTypePortRelative, vdslun/VDSStorageIdTypeSCSINameString, vdslun/VDSStorageIdTypeVendorId, vdslun/VDSStorageIdTypeVendorSpecific, vdslun/VDS_STORAGE_IDENTIFIER_TYPE
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
req.typenames: VDS_STORAGE_IDENTIFIER_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_STORAGE_IDENTIFIER_TYPE
 - vdslun/_VDS_STORAGE_IDENTIFIER_TYPE
 - VDS_STORAGE_IDENTIFIER_TYPE
 - vdslun/VDS_STORAGE_IDENTIFIER_TYPE
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
 - VDS_STORAGE_IDENTIFIER_TYPE
---

# VDS_STORAGE_IDENTIFIER_TYPE enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of valid types for a storage identifier.

## -enum-fields

### -field VDSStorageIdTypeVendorSpecific:0

The storage identifier type is vendor specific.

### -field VDSStorageIdTypeVendorId:1

The storage identifier is the same as the vendor identifier.

### -field VDSStorageIdTypeEUI64:2

The storage identifier type follows the IEEE 64-bit Extended Unique Identifier (EUI-64) standard.

### -field VDSStorageIdTypeFCPHName:3

The storage identifier type follows the Fibre Channel Physical and Signaling Interface (FC-PH) naming 
      convention.

### -field VDSStorageIdTypePortRelative:4

<b>VDS 1.1:  </b>The storage identifier type is dependent on the port.

### -field VDSStorageIdTypeTargetPortGroup:5

### -field VDSStorageIdTypeLogicalUnitGroup:6

### -field VDSStorageIdTypeMD5LogicalUnitIdentifier:7

### -field VDSStorageIdTypeScsiNameString:8

### -field VDSStorageIdTypeSCSINameString

<b>VDS 1.1:  </b>The storage identifier type follows the SCSI naming convention. See SCSI Primary Commands - 3 (SPC-3) for 
        more details.

## -remarks

The <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_storage_identifier">VDS_STORAGE_IDENTIFIER</a> structure 
    includes a <b>VDS_STORAGE_IDENTIFIER_TYPE</b> value as a member to indicate the storage identifier type.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_STORAGE_IDENTIFIER_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_STORAGE_IDENTIFIER_TYPE</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="/windows/desktop/api/vdslun/ns-vdslun-vds_storage_identifier">VDS_STORAGE_IDENTIFIER</a>
