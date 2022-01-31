---
UID: NE:vds._VDS_FILE_SYSTEM_TYPE
title: VDS_FILE_SYSTEM_TYPE (vds.h)
description: Defines the set of valid types for a file system.
helpviewer_keywords: ["VDS_FILE_SYSTEM_TYPE","VDS_FILE_SYSTEM_TYPE enumeration [VDS]","VDS_FST_CDFS","VDS_FST_EXFAT","VDS_FST_FAT","VDS_FST_FAT32","VDS_FST_NTFS","VDS_FST_RAW","VDS_FST_UDF","VDS_FST_UNKNOWN","base.vds_file_system_type","vds/VDS_FILE_SYSTEM_TYPE","vds/VDS_FST_CDFS","vds/VDS_FST_EXFAT","vds/VDS_FST_FAT","vds/VDS_FST_FAT32","vds/VDS_FST_NTFS","vds/VDS_FST_RAW","vds/VDS_FST_UDF","vds/VDS_FST_UNKNOWN","vdshwprv/VDS_FILE_SYSTEM_TYPE","vdshwprv/VDS_FST_CDFS","vdshwprv/VDS_FST_EXFAT","vdshwprv/VDS_FST_FAT","vdshwprv/VDS_FST_FAT32","vdshwprv/VDS_FST_NTFS","vdshwprv/VDS_FST_RAW","vdshwprv/VDS_FST_UDF","vdshwprv/VDS_FST_UNKNOWN"]
old-location: base\vds_file_system_type.htm
tech.root: base
ms.assetid: 56f2d969-eb1c-44c2-8a12-077a02ae40dc
ms.date: 12/05/2018
ms.keywords: VDS_FILE_SYSTEM_TYPE, VDS_FILE_SYSTEM_TYPE enumeration [VDS], VDS_FST_CDFS, VDS_FST_EXFAT, VDS_FST_FAT, VDS_FST_FAT32, VDS_FST_NTFS, VDS_FST_RAW, VDS_FST_UDF, VDS_FST_UNKNOWN, base.vds_file_system_type, vds/VDS_FILE_SYSTEM_TYPE, vds/VDS_FST_CDFS, vds/VDS_FST_EXFAT, vds/VDS_FST_FAT, vds/VDS_FST_FAT32, vds/VDS_FST_NTFS, vds/VDS_FST_RAW, vds/VDS_FST_UDF, vds/VDS_FST_UNKNOWN, vdshwprv/VDS_FILE_SYSTEM_TYPE, vdshwprv/VDS_FST_CDFS, vdshwprv/VDS_FST_EXFAT, vdshwprv/VDS_FST_FAT, vdshwprv/VDS_FST_FAT32, vdshwprv/VDS_FST_NTFS, vdshwprv/VDS_FST_RAW, vdshwprv/VDS_FST_UDF, vdshwprv/VDS_FST_UNKNOWN
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
req.typenames: VDS_FILE_SYSTEM_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_FILE_SYSTEM_TYPE
 - vds/_VDS_FILE_SYSTEM_TYPE
 - VDS_FILE_SYSTEM_TYPE
 - vds/VDS_FILE_SYSTEM_TYPE
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
 - VDS_FILE_SYSTEM_TYPE
---

# VDS_FILE_SYSTEM_TYPE enumeration


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of valid types for a file system.

## -enum-fields

### -field VDS_FST_UNKNOWN:0

The file system is unknown. The <a href="/windows/desktop/api/vds/nf-vds-ivdsvolumemf-getfilesystemproperties">IVdsVolumeMF::GetFileSystemProperties</a> method returns this value in the <a href="/windows/desktop/api/vds/ns-vds-vds_file_system_prop">VDS_FILE_SYSTEM_PROP</a> structure for BitLocker-encrypted volumes.

### -field VDS_FST_RAW

The file system is raw.

### -field VDS_FST_FAT

The file system is file allocation table (FAT).

### -field VDS_FST_FAT32

The file system is file allocation table for 32-bit computers (FAT32).

### -field VDS_FST_NTFS

The file system is the NT file system (NTFS).

### -field VDS_FST_CDFS

The file system is the CD-ROM file system (CDFS).

### -field VDS_FST_UDF

The file system is Universal Disk Format (UDF).

### -field VDS_FST_EXFAT

The file system is extended file allocation table (exFAT).

<b>Windows Server 2008, Windows Vista and Windows Server 2003:  </b>The VDS_FST_EXFAT file type value is not supported.

### -field VDS_FST_CSVFS

### -field VDS_FST_REFS

## -remarks

The <a href="/windows/desktop/api/vds/ns-vds-vds_file_system_prop">VDS_FILE_SYSTEM_PROP</a> structure includes a <b>VDS_FILE_SYSTEM_TYPE</b> value as a member to indicate an existing file system type.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_FILE_SYSTEM_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_FILE_SYSTEM_TYPE</b> enumeration constant.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsadvanceddisk-formatpartition">IVdsAdvancedDisk::FormatPartition</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsvolumemf-format">IVdsVolumeMF::Format</a>



<a href="/windows/desktop/api/vds/nf-vds-ivdsvolumemf-getfilesystemproperties">IVdsVolumeMF::GetFileSystemProperties</a>



<a href="/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_file_system_prop">VDS_FILE_SYSTEM_PROP</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_file_system_type_prop">VDS_FILE_SYSTEM_TYPE_PROP</a>



<a href="/windows/desktop/api/vds/ns-vds-vds_volume_prop">VDS_VOLUME_PROP</a>
