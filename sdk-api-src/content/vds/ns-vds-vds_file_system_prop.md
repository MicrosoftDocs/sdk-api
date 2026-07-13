---
UID: NS:vds._VDS_FILE_SYSTEM_PROP
title: VDS_FILE_SYSTEM_PROP (vds.h)
description: Defines the properties of a file system.
helpviewer_keywords: ["*PVDS_FILE_SYSTEM_PROP","PVDS_FILE_SYSTEM_PROP","PVDS_FILE_SYSTEM_PROP structure pointer [VDS]","VDS_FILE_SYSTEM_PROP","VDS_FILE_SYSTEM_PROP structure [VDS]","base.vds_file_system_prop","vds/PVDS_FILE_SYSTEM_PROP","vds/_VDS_FILE_SYSTEM_PROP"]
old-location: base\vds_file_system_prop.htm
tech.root: base
ms.assetid: 1068eb6d-0f7f-4d04-b7ec-f40e54ff8325
ms.date: 12/05/2018
ms.keywords: '*PVDS_FILE_SYSTEM_PROP, PVDS_FILE_SYSTEM_PROP, PVDS_FILE_SYSTEM_PROP structure pointer [VDS], VDS_FILE_SYSTEM_PROP, VDS_FILE_SYSTEM_PROP structure [VDS], base.vds_file_system_prop, vds/PVDS_FILE_SYSTEM_PROP, vds/_VDS_FILE_SYSTEM_PROP'
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
req.typenames: VDS_FILE_SYSTEM_PROP, *PVDS_FILE_SYSTEM_PROP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_FILE_SYSTEM_PROP
 - vds/_VDS_FILE_SYSTEM_PROP
 - PVDS_FILE_SYSTEM_PROP
 - vds/PVDS_FILE_SYSTEM_PROP
 - VDS_FILE_SYSTEM_PROP
 - vds/VDS_FILE_SYSTEM_PROP
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
 - VDS_FILE_SYSTEM_PROP
---

# VDS_FILE_SYSTEM_PROP structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Defines the properties of a file system.

## -struct-fields

### -field type

The file-system type enumerated by  <a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_file_system_type">VDS_FILE_SYSTEM_TYPE</a>.

### -field volumeId

The GUID of the volume object containing the file system.

### -field ulFlags

The file-system flags enumerated by <a href="/windows/desktop/api/vds/ne-vds-vds_file_system_prop_flag">VDS_FILE_SYSTEM_PROP_FLAG</a>.

### -field ullTotalAllocationUnits

The total number of allocation units.

### -field ullAvailableAllocationUnits

The  unused allocation units.

### -field ulAllocationUnitSize

The allocation unit size, in bytes, for the file system, which is
usually between 512 and 4096.

### -field pwszLabel

A string containing the file-system label.

## -remarks

The <a href="/windows/desktop/api/vds/nf-vds-ivdsvolumemf-getfilesystemproperties">IVdsVolumeMF::GetFileSystemProperties</a> method returns this structure to report the property details of a file system.

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsvolumemf-getfilesystemproperties">IVdsVolumeMF::GetFileSystemProperties</a>



<a href="/windows/desktop/VDS/vds-structures">VDS Structures</a>



<a href="/windows/desktop/api/vds/ne-vds-vds_file_system_prop_flag">VDS_FILE_SYSTEM_PROP_FLAG</a>



<a href="/windows/desktop/api/vdshwprv/ne-vdshwprv-vds_file_system_type">VDS_FILE_SYSTEM_TYPE</a>