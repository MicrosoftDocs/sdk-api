---
UID: NS:vds._VDS_DRIVE_LETTER_PROP
title: "_VDS_DRIVE_LETTER_PROP"
author: windows-sdk-content
description: Defines the properties of a drive letter.
old-location: base\vds_drive_letter_prop.htm
tech.root: VDS
ms.assetid: b944e29a-85b0-4cab-b804-1a09a19caddb
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PVDS_DRIVE_LETTER_PROP, PVDS_DRIVE_LETTER_PROP VDS_ASYNC_OUTPUT_TYPE, PVDS_DRIVE_LETTER_PROP VDS_ASYNC_OUTPUT_TYPE structure pointer [VDS], VDS_DRIVE_LETTER_PROP, VDS_DRIVE_LETTER_PROP structure [VDS], _VDS_DRIVE_LETTER_PROP, base.vds_drive_letter_prop, vds/PVDS_DRIVE_LETTER_PROP VDS_ASYNC_OUTPUT_TYPE, vds/_VDS_DRIVE_LETTER_PROP"
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
 - VDS_DRIVE_LETTER_PROP
product: Windows
targetos: Windows
req.typenames: VDS_DRIVE_LETTER_PROP, *PVDS_DRIVE_LETTER_PROP
req.redist: 
---

# _VDS_DRIVE_LETTER_PROP structure


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the properties of a drive letter.


## -struct-fields




### -field wcLetter

The drive letter.


### -field volumeId

The GUID of the volume object represented by the drive letter. 


### -field ulFlags

The drive letter flags enumerated by <a href="https://msdn.microsoft.com/f6eebe08-ebc9-45d3-a752-9cdc13f9bcf1">VDS_DRIVE_LETTER_FLAG</a>.


### -field bUsed

If true, the drive letter is already in use; otherwise, the drive letter is available.


## -remarks



The <a href="https://msdn.microsoft.com/e9e9f8b0-963f-4c57-9553-8b9241317b55">IVdsService::QueryDriveLetters</a> method returns this structure to report the property details of a drive letter.




## -see-also




<a href="https://msdn.microsoft.com/e9e9f8b0-963f-4c57-9553-8b9241317b55">IVdsService::QueryDriveLetters</a>



<a href="https://msdn.microsoft.com/6a13f5eb-0fa1-48e2-a112-b2254ca28423">VDS Structures</a>



<a href="https://msdn.microsoft.com/f6eebe08-ebc9-45d3-a752-9cdc13f9bcf1">VDS_DRIVE_LETTER_FLAG</a>
 

 

