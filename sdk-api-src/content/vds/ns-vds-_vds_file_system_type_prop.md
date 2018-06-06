---
UID: NS:vds._VDS_FILE_SYSTEM_TYPE_PROP
title: "_VDS_FILE_SYSTEM_TYPE_PROP"
author: windows-sdk-content
description: Defines the properties of a file system type.
old-location: base\vds_file_system_type_prop.htm
old-project: VDS
ms.assetid: 92383a59-d7dd-419b-b6d0-959fef41ad4e
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: "*PVDS_FILE_SYSTEM_TYPE_PROP, PVDS_FILE_SYSTEM_TYPE_PROP, PVDS_FILE_SYSTEM_TYPE_PROP structure pointer [VDS], VDS_FILE_SYSTEM_TYPE_PROP, VDS_FILE_SYSTEM_TYPE_PROP structure [VDS], _VDS_FILE_SYSTEM_TYPE_PROP, base.vds_file_system_type_prop, vds/PVDS_FILE_SYSTEM_TYPE_PROP, vds/_VDS_FILE_SYSTEM_TYPE_PROP"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: VDS_FILE_SYSTEM_TYPE_PROP, *PVDS_FILE_SYSTEM_TYPE_PROP
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vds.h
api_name:
 - VDS_FILE_SYSTEM_TYPE_PROP
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _VDS_FILE_SYSTEM_TYPE_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the properties of a file system type.


## -struct-fields




### -field type

The file system types enumerated by <a href="https://msdn.microsoft.com/56f2d969-eb1c-44c2-8a12-077a02ae40dc">VDS_FILE_SYSTEM_TYPE</a>. Valid types are FAT, FAT32, NTFS, CDFS and UDF.


### -field wszName

 The file system name.


### -field ulFlags

The file system flags enumerated by <a href="https://msdn.microsoft.com/2598877b-03f0-4190-8dcc-41ea3cb9497f">VDS_FILE_SYSTEM_FLAG</a>.


### -field ulCompressionFlags

The valid allocation unit sizes used for compression.


### -field ulMaxLableLength

The maximum length for a label name.


### -field pwszIllegalLabelCharSet

A string containing all characters that are not valid for this file system type.


## -remarks



The <a href="https://msdn.microsoft.com/17dcafc8-8faf-4dc2-af24-7e1ab257201e">IVdsService::QueryFileSystemTypes</a>
      method returns this structure to report the property details of a file-system type.




## -see-also




<a href="https://msdn.microsoft.com/17dcafc8-8faf-4dc2-af24-7e1ab257201e">IVdsService::QueryFileSystemTypes</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/2598877b-03f0-4190-8dcc-41ea3cb9497f">VDS_FILE_SYSTEM_FLAG</a>



<a href="https://msdn.microsoft.com/56f2d969-eb1c-44c2-8a12-077a02ae40dc">VDS_FILE_SYSTEM_TYPE</a>
 

 

