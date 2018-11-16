---
UID: NS:virtdisk._CREATE_VIRTUAL_DISK_PARAMETERS
title: "_CREATE_VIRTUAL_DISK_PARAMETERS"
author: windows-sdk-content
description: Contains virtual hard disk (VHD) creation parameters, providing control over, and information about, the newly created virtual disk.
old-location: vhd\create_virtual_disk_parameters.htm
tech.root: VStor
ms.assetid: 797e21ae-a4c4-48df-8124-e5c2fad22f33
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PCREATE_VIRTUAL_DISK_PARAMETERS, CREATE_VIRTUAL_DISK_PARAMETERS, CREATE_VIRTUAL_DISK_PARAMETERS structure [VHD], CREATE_VIRTUAL_DISK_PARAMETERS_DEFAULT_BLOCK_SIZE, CREATE_VIRTUAL_DISK_PARAMETERS_DEFAULT_SECTOR_SIZE, CREATE_VIRTUAL_DISK_VERSION_1, CREATE_VIRTUAL_DISK_VERSION_2, PCREATE_VIRTUAL_DISK_PARAMETERS, PCREATE_VIRTUAL_DISK_PARAMETERS structure pointer [VHD], _CREATE_VIRTUAL_DISK_PARAMETERS, vdssys/CREATE_VIRTUAL_DISK_PARAMETERS, vdssys/PCREATE_VIRTUAL_DISK_PARAMETERS, vhd.create_virtual_disk_parameters, virtdisk/CREATE_VIRTUAL_DISK_PARAMETERS, virtdisk/PCREATE_VIRTUAL_DISK_PARAMETERS"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: virtdisk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
 - VirtDisk.h
 - vdssys.h
api_name:
 - CREATE_VIRTUAL_DISK_PARAMETERS
product: Windows
targetos: Windows
req.typenames: CREATE_VIRTUAL_DISK_PARAMETERS, *PCREATE_VIRTUAL_DISK_PARAMETERS
req.redist: 
---

# _CREATE_VIRTUAL_DISK_PARAMETERS structure


## -description


Contains virtual hard disk (VHD) creation parameters, providing control over, and information about, 
    the newly created virtual disk.


## -struct-fields




### -field Version

A value from the <a href="https://msdn.microsoft.com/8a9f186a-88aa-43dc-97e0-2ffa43d7ffe5">CREATE_VIRTUAL_DISK_VERSION</a> 
      enumeration that is the discriminant for the union.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CREATE_VIRTUAL_DISK_VERSION_1"></a><a id="create_virtual_disk_version_1"></a><dl>
<dt><b>CREATE_VIRTUAL_DISK_VERSION_1</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Use the <b>Version1</b> member of this structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CREATE_VIRTUAL_DISK_VERSION_2"></a><a id="create_virtual_disk_version_2"></a><dl>
<dt><b>CREATE_VIRTUAL_DISK_VERSION_2</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Use the <b>Version2</b> member of this structure.

</td>
</tr>
</table>
 


### -field Version1

This structure is used if the <b>Version</b> member is 
       <b>CREATE_VIRTUAL_DISK_VERSION_1</b> (1).


### -field Version1.UniqueId

Unique identifier to assign to the virtual disk object. If this member is set to zero, a unique 
        identifier is created by the system.


### -field Version1.MaximumSize

The maximum virtual size, in bytes, of the virtual disk object. Must be a multiple of 512.

If a <b>ParentPath</b> is specified, this value must be zero.

If a <b>SourcePath</b> is specified, this value can be zero to specify the size of the 
         source virtual disk to be used, otherwise the size specified must be greater than or equal to the size of the 
         source disk.


### -field Version1.BlockSizeInBytes

Internal size of the virtual disk object blocks, in bytes. This must be set to 
        one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CREATE_VIRTUAL_DISK_PARAMETERS_DEFAULT_BLOCK_SIZE"></a><a id="create_virtual_disk_parameters_default_block_size"></a><dl>
<dt><b>CREATE_VIRTUAL_DISK_PARAMETERS_DEFAULT_BLOCK_SIZE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
This is the default value and represents a block size of 2 MB.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>524288 (0x80000)</dt>
</dl>
</td>
<td width="60%">
The block size is 512 KB.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2097152 (0x200000)</dt>
</dl>
</td>
<td width="60%">
The block size is 2 MB

</td>
</tr>
</table>
 


### -field Version1.SectorSizeInBytes

Internal size of the virtual disk object sectors. Must be set to 512.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CREATE_VIRTUAL_DISK_PARAMETERS_DEFAULT_SECTOR_SIZE"></a><a id="create_virtual_disk_parameters_default_sector_size"></a><dl>
<dt><b>CREATE_VIRTUAL_DISK_PARAMETERS_DEFAULT_SECTOR_SIZE</b></dt>
<dt>0x200</dt>
</dl>
</td>
<td width="60%">
The default and only allowable size, 512 bytes.

</td>
</tr>
</table>
 


### -field Version1.ParentPath

Optional <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">fully qualified</a> path to a parent 
         virtual disk object. Associates the new virtual disk with an existing virtual disk.

If this parameter is not <b>NULL</b>, <b>SourcePath</b> must be 
         <b>NULL</b>.


### -field Version1.SourcePath

Optional <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">fully qualified</a> path to 
          pre-populate the new virtual disk object with block data from an existing disk. This path may refer to a 
          virtual disk or a physical disk.

If this parameter is not <b>NULL</b>, <b>ParentPath</b> must be 
         <b>NULL</b>.


### -field Version2

This structure is used if the <b>Version</b> member is 
        <b>CREATE_VIRTUAL_DISK_VERSION_2</b> (2).

<b>Windows 7 and Windows Server 2008 R2:  </b>This structure is not supported until Windows 8 and Windows Server 2012.


### -field Version2.UniqueId

Unique identifier to assign to the virtual disk object. If this member is set to zero, a unique 
        identifier is created by the system.


### -field Version2.MaximumSize

The maximum virtual size, in bytes, of the virtual disk object. Must be a multiple of 512.

If a <b>ParentPath</b> is specified, this value must be zero.

If a <b>SourcePath</b> is specified, this value can be zero to specify the size of the 
         source virtual disk to be used, otherwise the size specified must be greater than or equal to the size of the 
         source disk.


### -field Version2.BlockSizeInBytes

Internal size of the virtual disk object blocks, in bytes. For VHDX this must be a multiple 
        of 1 MB between 1 and 256 MB. For VHD 1 this must be set to 
        one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CREATE_VIRTUAL_DISK_PARAMETERS_DEFAULT_BLOCK_SIZE"></a><a id="create_virtual_disk_parameters_default_block_size"></a><dl>
<dt><b>CREATE_VIRTUAL_DISK_PARAMETERS_DEFAULT_BLOCK_SIZE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
This is the default value and represents a block size of 2 MB. This is the only supported value for 
          fixed VHD 1 virtual disks.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>524288 (0x80000)</dt>
</dl>
</td>
<td width="60%">
The block size is 512 KB. This value is not supported on fixed VHD 1 virtual disks.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2097152 (0x200000)</dt>
</dl>
</td>
<td width="60%">
The block size is 2 MB. This value is not supported on fixed VHD 1 virtual disks.

</td>
</tr>
</table>
 


### -field Version2.SectorSizeInBytes

Internal size of the virtual disk object sectors. For VHDX  must be set to 512 (0x200) or 
        4096 (0x1000). For VHD 1 must be set to 512.


### -field Version2.PhysicalSectorSizeInBytes

 


### -field Version2.ParentPath

Optional <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">fully qualified</a> path to a parent 
         virtual disk object. Associates the new virtual disk with an existing virtual disk.

If this parameter is not <b>NULL</b>, <b>SourcePath</b> must be 
         <b>NULL</b>.


### -field Version2.SourcePath

Optional <a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">fully qualified</a> path to 
          pre-populate the new virtual disk object with block data from an existing disk. This path may refer to a 
          virtual disk or a physical disk.

If this parameter is not <b>NULL</b>, <b>ParentPath</b> must be 
         <b>NULL</b>.


### -field Version2.OpenFlags

Zero or more flags from the 
        <a href="https://msdn.microsoft.com/edc7d3ad-23a0-4e7a-82d5-8ac4df785f35">OPEN_VIRTUAL_DISK_FLAG</a> enumeration describing 
        how the virtual disk is to be opened.


### -field Version2.ParentVirtualStorageType

A <a href="https://msdn.microsoft.com/9f0c1848-fa8e-4747-a3b1-71a274695280">VIRTUAL_STORAGE_TYPE</a> structure describing 
        the parent virtual disk specified in the <b>ParentPath</b> member.


### -field Version2.SourceVirtualStorageType

A <a href="https://msdn.microsoft.com/9f0c1848-fa8e-4747-a3b1-71a274695280">VIRTUAL_STORAGE_TYPE</a> structure describing 
        the source virtual disk specified in the <b>SourcePath</b> member.


### -field Version2.ResiliencyGuid

Resiliency <b>GUID</b> for the file.


### -field Version3

 


### -field Version3.UniqueId

 


### -field Version3.MaximumSize

 


### -field Version3.BlockSizeInBytes

 


### -field Version3.SectorSizeInBytes

 


### -field Version3.PhysicalSectorSizeInBytes

 


### -field Version3.ParentPath

 


### -field Version3.SourcePath

 


### -field Version3.OpenFlags

 


### -field Version3.ParentVirtualStorageType

 


### -field Version3.SourceVirtualStorageType

 


### -field Version3.ResiliencyGuid

 


### -field Version3.SourceLimitPath

 


### -field Version3.BackingStorageType

 


### -field Version4

 


### -field Version4.UniqueId

 


### -field Version4.MaximumSize

 


### -field Version4.BlockSizeInBytes

 


### -field Version4.SectorSizeInBytes

 


### -field Version4.PhysicalSectorSizeInBytes

 


### -field Version4.ParentPath

 


### -field Version4.SourcePath

 


### -field Version4.OpenFlags

 


### -field Version4.ParentVirtualStorageType

 


### -field Version4.SourceVirtualStorageType

 


### -field Version4.ResiliencyGuid

 


### -field Version4.SourceLimitPath

 


### -field Version4.BackingStorageType

 


### -field Version4.PmemAddressAbstractionType

 


### -field Version4.DataAlignment

 




## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/9d9f187e-dea1-48ca-a3fe-9e9c513e9088">CreateVirtualDisk</a>



<a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming Files, Paths, and Namespaces</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>



<a href="https://msdn.microsoft.com/e0caf715-bde5-4fe8-ad69-9372146e17b9">VHD Structures</a>
 

 

