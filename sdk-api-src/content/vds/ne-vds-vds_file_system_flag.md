---
UID: NE:vds._VDS_FILE_SYSTEM_FLAG
title: VDS_FILE_SYSTEM_FLAG (vds.h)
description: Defines the set of valid flags for a file system.
old-location: base\vds_file_system_flag.htm
tech.root: VDS
ms.assetid: 2598877b-03f0-4190-8dcc-41ea3cb9497f
ms.date: 12/05/2018
ms.keywords: VDS_FILE_SYSTEM_FLAG, VDS_FILE_SYSTEM_FLAG enumeration [VDS], VDS_FSF_ALLOCATION_UNIT_128K, VDS_FSF_ALLOCATION_UNIT_16K, VDS_FSF_ALLOCATION_UNIT_1K, VDS_FSF_ALLOCATION_UNIT_256K, VDS_FSF_ALLOCATION_UNIT_2K, VDS_FSF_ALLOCATION_UNIT_32K, VDS_FSF_ALLOCATION_UNIT_4K, VDS_FSF_ALLOCATION_UNIT_512, VDS_FSF_ALLOCATION_UNIT_64K, VDS_FSF_ALLOCATION_UNIT_8K, VDS_FSF_SUPPORT_COMPRESS, VDS_FSF_SUPPORT_EXTEND, VDS_FSF_SUPPORT_FORMAT, VDS_FSF_SUPPORT_MOUNT_POINT, VDS_FSF_SUPPORT_QUICK_FORMAT, VDS_FSF_SUPPORT_REMOVABLE_MEDIA, VDS_FSF_SUPPORT_SPECIFY_LABEL, base.vds_file_system_flag, vds/VDS_FILE_SYSTEM_FLAG, vds/VDS_FSF_ALLOCATION_UNIT_128K, vds/VDS_FSF_ALLOCATION_UNIT_16K, vds/VDS_FSF_ALLOCATION_UNIT_1K, vds/VDS_FSF_ALLOCATION_UNIT_256K, vds/VDS_FSF_ALLOCATION_UNIT_2K, vds/VDS_FSF_ALLOCATION_UNIT_32K, vds/VDS_FSF_ALLOCATION_UNIT_4K, vds/VDS_FSF_ALLOCATION_UNIT_512, vds/VDS_FSF_ALLOCATION_UNIT_64K, vds/VDS_FSF_ALLOCATION_UNIT_8K, vds/VDS_FSF_SUPPORT_COMPRESS, vds/VDS_FSF_SUPPORT_EXTEND, vds/VDS_FSF_SUPPORT_FORMAT, vds/VDS_FSF_SUPPORT_MOUNT_POINT, vds/VDS_FSF_SUPPORT_QUICK_FORMAT, vds/VDS_FSF_SUPPORT_REMOVABLE_MEDIA, vds/VDS_FSF_SUPPORT_SPECIFY_LABEL
ms.topic: enum
f1_keywords:
- vds/VDS_FILE_SYSTEM_FLAG
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Vds.h
api_name:
- VDS_FILE_SYSTEM_FLAG
targetos: Windows
req.typenames: VDS_FILE_SYSTEM_FLAG
req.redist: 
ms.custom: 19H1
---

# VDS_FILE_SYSTEM_FLAG enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://docs.microsoft.com/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the set of valid flags for a file system.


## -enum-fields




### -field VDS_FSF_SUPPORT_FORMAT

If set, the file system supports format. The drop-down list of a user interface should display only file systems that support formatting.


### -field VDS_FSF_SUPPORT_QUICK_FORMAT

If set, the file system supports quick format.


### -field VDS_FSF_SUPPORT_COMPRESS

If set, the file system supports file compression.


### -field VDS_FSF_SUPPORT_SPECIFY_LABEL

If set, the file system supports file system labels.


### -field VDS_FSF_SUPPORT_MOUNT_POINT

If set, the file system supports mounted folders.


### -field VDS_FSF_SUPPORT_REMOVABLE_MEDIA

If set, the file system supports removable media.


### -field VDS_FSF_SUPPORT_EXTEND

If set, the file system supports extending volumes.


### -field VDS_FSF_ALLOCATION_UNIT_512

If set, the file system supports allocation units of 512 bytes.


### -field VDS_FSF_ALLOCATION_UNIT_1K

If set, the file system supports allocation units of 1 kilobyte.


### -field VDS_FSF_ALLOCATION_UNIT_2K

If set, the file system supports allocation units of 2 kilobytes.


### -field VDS_FSF_ALLOCATION_UNIT_4K

If set, the file system supports allocation units of 4 kilobytes.


### -field VDS_FSF_ALLOCATION_UNIT_8K

If set, the file system supports allocation units of 8 kilobytes.


### -field VDS_FSF_ALLOCATION_UNIT_16K

If set, the file system supports allocation units of 16 kilobytes.


### -field VDS_FSF_ALLOCATION_UNIT_32K

If set, the file system supports allocation units of 32 kilobytes.


### -field VDS_FSF_ALLOCATION_UNIT_64K

If set, the file system supports allocation units of 64 kilobytes.


### -field VDS_FSF_ALLOCATION_UNIT_128K

If set, the file system supports allocation units of 128 kilobytes.


### -field VDS_FSF_ALLOCATION_UNIT_256K

If set, the file system supports allocation units of 256 kilobytes.


## -remarks



This enumeration provides the values for the <i>ulFlags</i> member of the <a href="https://docs.microsoft.com/windows/desktop/api/vds/ns-vds-vds_file_system_prop">VDS_FILE_SYSTEM_PROP</a>structure. The <a href="https://docs.microsoft.com/windows/desktop/api/vds/nf-vds-ivdsvolumemf-setfilesystemflags">SetFileSystemFlags</a> method passes the value as an argument to set the <b>VDS_FPF_COMPRESSED</b> flag.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_FILE_SYSTEM_FLAG</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_FILE_SYSTEM_FLAG</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/VDS/vds-enumerations">VDS Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/vds/ns-vds-vds_file_system_prop">VDS_FILE_SYSTEM_PROP</a>
 

 

