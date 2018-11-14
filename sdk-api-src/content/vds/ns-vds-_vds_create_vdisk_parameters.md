---
UID: NS:vds._VDS_CREATE_VDISK_PARAMETERS
title: "_VDS_CREATE_VDISK_PARAMETERS"
author: windows-sdk-content
description: Contains the parameters to be used when a virtual disk is created.
old-location: base\vds_create_vdisk_parameters.htm
tech.root: VDS
ms.assetid: 7ee830d5-6392-4e66-a8bb-2fd92c1e092c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PVDS_CREATE_VDISK_PARAMETERS, PVDS_CREATE_VDISK_PARAMETERS, PVDS_CREATE_VDISK_PARAMETERS structure pointer, VDS_CREATE_VDISK_PARAMETERS, VDS_CREATE_VDISK_PARAMETERS structure, _VDS_CREATE_VDISK_PARAMETERS, base.vds_create_vdisk_parameters, vds/PVDS_CREATE_VDISK_PARAMETERS, vds/VDS_CREATE_VDISK_PARAMETERS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
api_name:
 - VDS_CREATE_VDISK_PARAMETERS
product: Windows
targetos: Windows
req.typenames: VDS_CREATE_VDISK_PARAMETERS, *PVDS_CREATE_VDISK_PARAMETERS
req.redist: 
---

# _VDS_CREATE_VDISK_PARAMETERS structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

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




<a href="https://msdn.microsoft.com/3655946d-f8b5-46a1-97e3-82b0831124b3">IVdsVdProvider::CreateVDisk</a>
 

 

