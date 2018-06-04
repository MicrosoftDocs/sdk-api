---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _VDS_FILE_SYSTEM_TYPE enumeration


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines the set of valid types for a file system.


## -enum-fields




### -field VDS_FST_UNKNOWN

The file system is unknown. The <a href="https://msdn.microsoft.com/43f5495c-5a60-44fd-b217-16464c4693a4">IVdsVolumeMF::GetFileSystemProperties</a> method returns this value in the <a href="https://msdn.microsoft.com/1068eb6d-0f7f-4d04-b7ec-f40e54ff8325">VDS_FILE_SYSTEM_PROP</a> structure for BitLocker-encrypted volumes.


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



The <a href="https://msdn.microsoft.com/1068eb6d-0f7f-4d04-b7ec-f40e54ff8325">VDS_FILE_SYSTEM_PROP</a>
        structure includes a <b>VDS_FILE_SYSTEM_TYPE</b> value as a member to indicate an existing file system type.

<div class="alert"><b>Note</b>  Additional constants might be added to the <b>VDS_FILE_SYSTEM_TYPE</b> enumeration in future Windows versions. For this reason, your application must be designed to gracefully handle an unrecognized <b>VDS_FILE_SYSTEM_TYPE</b> enumeration constant.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/9b7015c2-a85d-4a56-8aec-208933640185">
        IVdsAdvancedDisk::FormatPartition</a>



<a href="https://msdn.microsoft.com/8203ac16-99af-4962-bafc-12c0d238d062">
        IVdsVolumeMF::Format</a>



<a href="https://msdn.microsoft.com/43f5495c-5a60-44fd-b217-16464c4693a4">IVdsVolumeMF::GetFileSystemProperties</a>



<a href="https://msdn.microsoft.com/30ee6e39-c1e5-4173-a3dd-5644632140d1">VDS Enumerations</a>



<a href="https://msdn.microsoft.com/1068eb6d-0f7f-4d04-b7ec-f40e54ff8325">
        VDS_FILE_SYSTEM_PROP</a>



<a href="https://msdn.microsoft.com/92383a59-d7dd-419b-b6d0-959fef41ad4e">
        VDS_FILE_SYSTEM_TYPE_PROP</a>



<a href="https://msdn.microsoft.com/3628b312-f830-4a1c-beb7-ad002a94313c">
        VDS_VOLUME_PROP</a>
 

 

