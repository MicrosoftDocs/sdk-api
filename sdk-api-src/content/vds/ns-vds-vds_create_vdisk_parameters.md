---
UID: NS:vds._VDS_CREATE_VDISK_PARAMETERS
title: VDS_CREATE_VDISK_PARAMETERS (vds.h)
description: Contains the parameters to be used when a virtual disk is created.
helpviewer_keywords: ["*PVDS_CREATE_VDISK_PARAMETERS","PVDS_CREATE_VDISK_PARAMETERS","PVDS_CREATE_VDISK_PARAMETERS structure pointer","VDS_CREATE_VDISK_PARAMETERS","VDS_CREATE_VDISK_PARAMETERS structure","base.vds_create_vdisk_parameters","vds/PVDS_CREATE_VDISK_PARAMETERS","vds/VDS_CREATE_VDISK_PARAMETERS"]
old-location: base\vds_create_vdisk_parameters.htm
tech.root: base
ms.assetid: 7ee830d5-6392-4e66-a8bb-2fd92c1e092c
ms.date: 12/05/2018
ms.keywords: '*PVDS_CREATE_VDISK_PARAMETERS, PVDS_CREATE_VDISK_PARAMETERS, PVDS_CREATE_VDISK_PARAMETERS structure pointer, VDS_CREATE_VDISK_PARAMETERS, VDS_CREATE_VDISK_PARAMETERS structure, base.vds_create_vdisk_parameters, vds/PVDS_CREATE_VDISK_PARAMETERS, vds/VDS_CREATE_VDISK_PARAMETERS'
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: VDS_CREATE_VDISK_PARAMETERS, *PVDS_CREATE_VDISK_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VDS_CREATE_VDISK_PARAMETERS
 - vds/_VDS_CREATE_VDISK_PARAMETERS
 - PVDS_CREATE_VDISK_PARAMETERS
 - vds/PVDS_CREATE_VDISK_PARAMETERS
 - VDS_CREATE_VDISK_PARAMETERS
 - vds/VDS_CREATE_VDISK_PARAMETERS
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
 - VDS_CREATE_VDISK_PARAMETERS
---

# VDS_CREATE_VDISK_PARAMETERS structure


## -description

<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="/windows/desktop/VDS/virtual-disk-service-portal">Virtual Disk Service</a> COM interface is superseded by the <a href="/windows-hardware/drivers/storage/windows-storage-management-api-portal">Windows Storage Management API</a>.]

Contains the parameters to be used when a virtual disk is created.

## -struct-fields

### -field UniqueId

A unique GUID value to be assigned to the virtual disk.

### -field MaximumSize

The maximum virtual size, in bytes, of the virtual disk object.

### -field BlockSizeInBytes

The internal block size, in bytes, of the virtual disk object.

### -field SectorSizeInBytes

Internal sector size, in bytes, of the virtual disk object.

### -field pParentPath

A <b>NULL</b>-terminated wide-character string that contains an optional path to a parent virtual disk object. This member associates the new virtual disk with an existing virtual disk.

### -field pSourcePath

A <b>NULL</b>-terminated wide-character string that contains an optional path to a source of data to be copied to the new virtual disk.

## -see-also

<a href="/windows/desktop/api/vds/nf-vds-ivdsvdprovider-createvdisk">IVdsVdProvider::CreateVDisk</a>