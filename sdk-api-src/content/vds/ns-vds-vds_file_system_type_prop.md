---
UID: NS:vds._VDS_FILE_SYSTEM_TYPE_PROP
title: VDS_FILE_SYSTEM_TYPE_PROP (vds.h)
description: Defines the properties of a file system type.
helpviewer_keywords: ["*PVDS_FILE_SYSTEM_TYPE_PROP","PVDS_FILE_SYSTEM_TYPE_PROP","PVDS_FILE_SYSTEM_TYPE_PROP structure pointer [VDS]","VDS_FILE_SYSTEM_TYPE_PROP","VDS_FILE_SYSTEM_TYPE_PROP structure [VDS]","base.vds_file_system_type_prop","vds/PVDS_FILE_SYSTEM_TYPE_PROP","vds/_VDS_FILE_SYSTEM_TYPE_PROP"]
old-location: base\vds_file_system_type_prop.htm
tech.root: base
ms.assetid: 92383a59-d7dd-419b-b6d0-959fef41ad4e
ms.date: 12/05/2018
ms.keywords: '*PVDS_FILE_SYSTEM_TYPE_PROP, PVDS_FILE_SYSTEM_TYPE_PROP, PVDS_FILE_SYSTEM_TYPE_PROP structure pointer [VDS], VDS_FILE_SYSTEM_TYPE_PROP, VDS_FILE_SYSTEM_TYPE_PROP structure [VDS], base.vds_file_system_type_prop, vds/PVDS_FILE_SYSTEM_TYPE_PROP, vds/_VDS_FILE_SYSTEM_TYPE_PROP'
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
req.typenames: VDS_FILE_SYSTEM_TYPE_PROP, *PVDS_FILE_SYSTEM_TYPE_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_FILE_SYSTEM_TYPE_PROP
 - vds/_VDS_FILE_SYSTEM_TYPE_PROP
 - PVDS_FILE_SYSTEM_TYPE_PROP
 - vds/PVDS_FILE_SYSTEM_TYPE_PROP
 - VDS_FILE_SYSTEM_TYPE_PROP
 - vds/VDS_FILE_SYSTEM_TYPE_PROP
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
api_name:
 - VDS_FILE_SYSTEM_TYPE_PROP
---

# VDS_FILE_SYSTEM_TYPE_PROP structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the properties of a file system type.

## -struct-fields

### -field type

The file system types enumerated by <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_file_system_type">VDS_FILE_SYSTEM_TYPE</a>. Valid types are FAT, FAT32, NTFS, CDFS and UDF.

### -field wszName

 The file system name.

### -field ulFlags

The file system flags enumerated by <a href="/windows/desktop/api/vds/ne-vds-vds_file_system_flag">VDS_FILE_SYSTEM_FLAG</a>.

### -field ulCompressionFlags

The valid allocation unit sizes used for compression.

### -field ulMaxLableLength

The maximum length for a label name.

### -field pwszIllegalLabelCharSet

A string containing all characters that are not valid for this file system type.

## -remarks

The <a href="/windows/desktop/api/vds/nf-vds-ivdsservice-queryfilesystemtypes">IVdsService::QueryFileSystemTypes</a> method returns this structure to report the property details of a file-system type.

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsservice-queryfilesystemtypes">IVdsService::QueryFileSystemTypes</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_file_system_flag">VDS_FILE_SYSTEM_FLAG</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_file_system_type">VDS_FILE_SYSTEM_TYPE</a>