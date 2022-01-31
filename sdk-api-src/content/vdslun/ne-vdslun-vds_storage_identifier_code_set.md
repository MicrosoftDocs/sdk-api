---
UID: NE:vdslun._VDS_STORAGE_IDENTIFIER_CODE_SET
title: VDS_STORAGE_IDENTIFIER_CODE_SET (vdslun.h)
description: Defines the set of the valid code sets (encodings) of a storage identifier.
helpviewer_keywords: ["VDSStorageIdCodeSetAscii","VDSStorageIdCodeSetBinary","VDSStorageIdCodeSetReserved","VDSStorageIdCodeSetUtf8","VDS_STORAGE_IDENTIFIER_CODE_SET","VDS_STORAGE_IDENTIFIER_CODE_SET enumeration [VDS]","base.vds_storage_identifier_code_set","vdslun/VDSStorageIdCodeSetAscii","vdslun/VDSStorageIdCodeSetBinary","vdslun/VDSStorageIdCodeSetReserved","vdslun/VDSStorageIdCodeSetUtf8","vdslun/VDS_STORAGE_IDENTIFIER_CODE_SET"]
old-location: base\vds_storage_identifier_code_set.htm
tech.root: base
ms.assetid: 6b4a3282-dc0c-4974-8c4c-777a28fb9005
ms.date: 12/05/2018
ms.keywords: VDSStorageIdCodeSetAscii, VDSStorageIdCodeSetBinary, VDSStorageIdCodeSetReserved, VDSStorageIdCodeSetUtf8, VDS_STORAGE_IDENTIFIER_CODE_SET, VDS_STORAGE_IDENTIFIER_CODE_SET enumeration [VDS], base.vds_storage_identifier_code_set, vdslun/VDSStorageIdCodeSetAscii, vdslun/VDSStorageIdCodeSetBinary, vdslun/VDSStorageIdCodeSetReserved, vdslun/VDSStorageIdCodeSetUtf8, vdslun/VDS_STORAGE_IDENTIFIER_CODE_SET
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
req.typenames: VDS_STORAGE_IDENTIFIER_CODE_SET
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_STORAGE_IDENTIFIER_CODE_SET
 - vdslun/_VDS_STORAGE_IDENTIFIER_CODE_SET
 - VDS_STORAGE_IDENTIFIER_CODE_SET
 - vdslun/VDS_STORAGE_IDENTIFIER_CODE_SET
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
 - VDS_STORAGE_IDENTIFIER_CODE_SET
---

# VDS_STORAGE_IDENTIFIER_CODE_SET enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of the valid code sets (encodings) of a storage identifier.

## -enum-fields

### -field VDSStorageIdCodeSetReserved:0

This value is reserved.

### -field VDSStorageIdCodeSetBinary:1

The storage identifier is encoded as binary data.

### -field VDSStorageIdCodeSetAscii:2

The storage identifier is encoded as ASCII data.

### -field VDSStorageIdCodeSetUtf8:3

The storage identifier is encoded as UTF-8.

<b>Windows Vista and Windows Server 2003:  </b>Not supported before Windows Vista with SP1 and Windows Server 2008.

## -remarks

The <a href="/windows/desktop/api/vdslun/ns-vdslun-vds_storage_identifier">VDS_STORAGE_IDENTIFIER</a> structure includes 
    a <b>VDS_STORAGE_IDENTIFIER_CODE_SET</b> value as a member to indicate the code set of a storage identifier.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_STORAGE_IDENTIFIER_CODE_SET</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_STORAGE_IDENTIFIER_CODE_SET</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="/windows/desktop/api/vdslun/ns-vdslun-vds_storage_identifier">VDS_STORAGE_IDENTIFIER</a>
