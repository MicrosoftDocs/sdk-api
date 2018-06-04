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

# _FILESYSTEM_STATISTICS_EX structure


## -description


Contains statistical information from the file system.Support for this structure started with Windows 10.




## -struct-fields




### -field FileSystemType

The type of file system.

This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILESYSTEM_STATISTICS_TYPE_EXFAT"></a><a id="filesystem_statistics_type_exfat"></a><dl>
<dt><b>FILESYSTEM_STATISTICS_TYPE_EXFAT</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The file system is an exFAT file system.

If this value is set, this structure is followed by an 
         <a href="https://msdn.microsoft.com/fc33e967-fbc0-4f98-9b6c-2d6ac103a256">EXFAT_STATISTICS</a> structure.

<b>Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Vista with SP1.

</td>
</tr>
<tr>
<td width="40%"><a id="FILESYSTEM_STATISTICS_TYPE_FAT"></a><a id="filesystem_statistics_type_fat"></a><dl>
<dt><b>FILESYSTEM_STATISTICS_TYPE_FAT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The file system is a FAT file system.

If this value is set, this structure is followed by a 
         <a href="https://msdn.microsoft.com/98d293e8-e708-48f5-99b1-603f27e6ef16">FAT_STATISTICS</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="FILESYSTEM_STATISTICS_TYPE_NTFS"></a><a id="filesystem_statistics_type_ntfs"></a><dl>
<dt><b>FILESYSTEM_STATISTICS_TYPE_NTFS</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The file system is the NTFS file system.

If this value is set, this structure is followed by an 
         <a href="https://msdn.microsoft.com/D1A6995C-A4BA-4ECC-892A-196581FA41CE">NTFS_STATISTICS_EX</a> structure.

</td>
</tr>
</table>
 


### -field Version

This member is set to 1 (one).


### -field SizeOfCompleteStructure

The size of this structure plus the size of the file system-specific structure that follows this 
       structure, multiplied by the number of processors.

This value must be a multiple of 64. For example, if the size of 
       <b>FILESYSTEM_STATISTICS_EX</b> is 0x68, the size of 
       <a href="https://msdn.microsoft.com/D1A6995C-A4BA-4ECC-892A-196581FA41CE">NTFS_STATISTICS_EX</a> is 0x1D8, and if there are 2 
       processors, the buffer allocated must be 0x480.

sizeof(<b>FILESYSTEM_STATISTICS_EX</b>) = 
       0x68

sizeof(<a href="https://msdn.microsoft.com/D1A6995C-A4BA-4ECC-892A-196581FA41CE">NTFS_STATISTICS_EX</a>) = 0x1D8

Total Size = 0x240

size of the complete structure = 0x240 (which is the aligned length, a multiple of 64)

multiplied by 2 (the number of processors) = 0x480


### -field UserFileReads

The number of read operations on user files.


### -field UserFileReadBytes

The number of bytes read from user files.


### -field UserDiskReads

The number of read operations on user files.

This value includes sub-read operations.


### -field UserFileWrites

The number of write operations on user files.


### -field UserFileWriteBytes

The number of bytes written to user files.


### -field UserDiskWrites

The number of write operations on user files.

This value includes sub-write operations.


### -field MetaDataReads

The number of read operations on metadata files.


### -field MetaDataReadBytes

The number of bytes read from metadata files.


### -field MetaDataDiskReads

The number of read operations on metadata files.

This value includes sub-read operations.


### -field MetaDataWrites

The number of write operations on metadata files.


### -field MetaDataWriteBytes

The number of bytes written to metadata files.


### -field MetaDataDiskWrites

The number of write operations on metadata files.

This value includes sub-write operations.


## -remarks



There are two types of files: user and metadata. User files are available for the user. Metadata files are 
    system files that contain information, which the file system uses for its internal organization.

The number of read and write operations measured is the number of paging operations.




## -see-also




<a href="https://msdn.microsoft.com/fc33e967-fbc0-4f98-9b6c-2d6ac103a256">EXFAT_STATISTICS</a>



<a href="https://msdn.microsoft.com/98d293e8-e708-48f5-99b1-603f27e6ef16">FAT_STATISTICS</a>



<a href="https://msdn.microsoft.com/d975d32c-1290-4397-8c05-6c515af4c450">FSCTL_FILESYSTEM_GET_STATISTICS</a>



<a href="https://msdn.microsoft.com/D1A6995C-A4BA-4ECC-892A-196581FA41CE">NTFS_STATISTICS_EX</a>
 

 

