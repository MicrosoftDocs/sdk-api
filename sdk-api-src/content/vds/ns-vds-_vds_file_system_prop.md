---
UID: NS:vds._VDS_FILE_SYSTEM_PROP
title: "_VDS_FILE_SYSTEM_PROP"
author: windows-sdk-content
description: Defines the properties of a file system.
old-location: base\vds_file_system_prop.htm
old-project: VDS
ms.assetid: 1068eb6d-0f7f-4d04-b7ec-f40e54ff8325
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PVDS_FILE_SYSTEM_PROP, PVDS_FILE_SYSTEM_PROP, PVDS_FILE_SYSTEM_PROP structure pointer [VDS], VDS_FILE_SYSTEM_PROP, VDS_FILE_SYSTEM_PROP structure [VDS], _VDS_FILE_SYSTEM_PROP, base.vds_file_system_prop, vds/PVDS_FILE_SYSTEM_PROP, vds/_VDS_FILE_SYSTEM_PROP"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: vds.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: VDS_FILE_SYSTEM_PROP, *PVDS_FILE_SYSTEM_PROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
api_name:
 - VDS_FILE_SYSTEM_PROP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_FILE_SYSTEM_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the properties of a file system.


## -struct-fields




### -field type

The file-system type enumerated by  <a href="https://msdn.microsoft.com/56f2d969-eb1c-44c2-8a12-077a02ae40dc">VDS_FILE_SYSTEM_TYPE</a>.


### -field volumeId

The GUID of the volume object containing the file system.


### -field ulFlags

The file-system flags enumerated by <a href="https://msdn.microsoft.com/f2776ee9-4809-4f99-b464-80b5b53f8675">VDS_FILE_SYSTEM_PROP_FLAG</a>.


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



The <a href="https://msdn.microsoft.com/43f5495c-5a60-44fd-b217-16464c4693a4">IVdsVolumeMF::GetFileSystemProperties</a>method returns this structure to report the property details of a file system.




## -see-also




<a href="https://msdn.microsoft.com/43f5495c-5a60-44fd-b217-16464c4693a4">IVdsVolumeMF::GetFileSystemProperties</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/f2776ee9-4809-4f99-b464-80b5b53f8675">VDS_FILE_SYSTEM_PROP_FLAG</a>



<a href="https://msdn.microsoft.com/56f2d969-eb1c-44c2-8a12-077a02ae40dc">VDS_FILE_SYSTEM_TYPE</a>
 

 

