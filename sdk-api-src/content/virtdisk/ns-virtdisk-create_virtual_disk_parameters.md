---
UID: NS:virtdisk._CREATE_VIRTUAL_DISK_PARAMETERS
title: CREATE_VIRTUAL_DISK_PARAMETERS (virtdisk.h)
description: Contains virtual hard disk (VHD) creation parameters, providing control over, and information about, the newly created virtual disk.
helpviewer_keywords: ["*PCREATE_VIRTUAL_DISK_PARAMETERS","CREATE_VIRTUAL_DISK_PARAMETERS","CREATE_VIRTUAL_DISK_PARAMETERS structure [VHD]","CREATE_VIRTUAL_DISK_PARAMETERS_DEFAULT_BLOCK_SIZE","CREATE_VIRTUAL_DISK_PARAMETERS_DEFAULT_SECTOR_SIZE","CREATE_VIRTUAL_DISK_VERSION_1","CREATE_VIRTUAL_DISK_VERSION_2","PCREATE_VIRTUAL_DISK_PARAMETERS","PCREATE_VIRTUAL_DISK_PARAMETERS structure pointer [VHD]","_CREATE_VIRTUAL_DISK_PARAMETERS","vdssys/CREATE_VIRTUAL_DISK_PARAMETERS","vdssys/PCREATE_VIRTUAL_DISK_PARAMETERS","vhd.create_virtual_disk_parameters","virtdisk/CREATE_VIRTUAL_DISK_PARAMETERS","virtdisk/PCREATE_VIRTUAL_DISK_PARAMETERS"]
old-location: vhd\create_virtual_disk_parameters.htm
tech.root: VStor
ms.assetid: 797e21ae-a4c4-48df-8124-e5c2fad22f33
ms.date: 07/28/2020
ms.keywords: '*PCREATE_VIRTUAL_DISK_PARAMETERS, CREATE_VIRTUAL_DISK_PARAMETERS, CREATE_VIRTUAL_DISK_PARAMETERS structure [VHD], CREATE_VIRTUAL_DISK_PARAMETERS_DEFAULT_BLOCK_SIZE, CREATE_VIRTUAL_DISK_PARAMETERS_DEFAULT_SECTOR_SIZE, CREATE_VIRTUAL_DISK_VERSION_1, CREATE_VIRTUAL_DISK_VERSION_2, PCREATE_VIRTUAL_DISK_PARAMETERS, PCREATE_VIRTUAL_DISK_PARAMETERS structure pointer [VHD], _CREATE_VIRTUAL_DISK_PARAMETERS, vdssys/CREATE_VIRTUAL_DISK_PARAMETERS, vdssys/PCREATE_VIRTUAL_DISK_PARAMETERS, vhd.create_virtual_disk_parameters, virtdisk/CREATE_VIRTUAL_DISK_PARAMETERS, virtdisk/PCREATE_VIRTUAL_DISK_PARAMETERS'
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
targetos: Windows
req.typenames: CREATE_VIRTUAL_DISK_PARAMETERS, *PCREATE_VIRTUAL_DISK_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CREATE_VIRTUAL_DISK_PARAMETERS
 - virtdisk/_CREATE_VIRTUAL_DISK_PARAMETERS
 - PCREATE_VIRTUAL_DISK_PARAMETERS
 - virtdisk/PCREATE_VIRTUAL_DISK_PARAMETERS
 - CREATE_VIRTUAL_DISK_PARAMETERS
 - virtdisk/CREATE_VIRTUAL_DISK_PARAMETERS
dev_langs:
 - c++
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
---

# CREATE_VIRTUAL_DISK_PARAMETERS structure


## -description

Contains virtual hard disk (VHD) creation parameters, providing control over, and information about, 
    the newly created virtual disk.

## -struct-fields

### -field Version

A value from the <a href="/windows/win32/api/virtdisk/ne-virtdisk-create_virtual_disk_version">CREATE_VIRTUAL_DISK_VERSION</a> 
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

Optional <a href="/windows/desktop/FileIO/naming-a-file">fully qualified</a> path to a parent 
         virtual disk object. Associates the new virtual disk with an existing virtual disk.

If this parameter is not <b>NULL</b>, <b>SourcePath</b> must be 
         <b>NULL</b>.

### -field Version1.SourcePath

Optional <a href="/windows/desktop/FileIO/naming-a-file">fully qualified</a> path to 
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

Optional <a href="/windows/desktop/FileIO/naming-a-file">fully qualified</a> path to a parent 
         virtual disk object. Associates the new virtual disk with an existing virtual disk.

If this parameter is not <b>NULL</b>, <b>SourcePath</b> must be 
         <b>NULL</b>.

### -field Version2.SourcePath

Optional <a href="/windows/desktop/FileIO/naming-a-file">fully qualified</a> path to 
          pre-populate the new virtual disk object with block data from an existing disk. This path may refer to a 
          virtual disk or a physical disk.

If this parameter is not <b>NULL</b>, <b>ParentPath</b> must be 
         <b>NULL</b>.

### -field Version2.OpenFlags

Zero or more flags from the 
        <a href="/windows/win32/api/virtdisk/ne-virtdisk-open_virtual_disk_flag">OPEN_VIRTUAL_DISK_FLAG</a> enumeration describing 
        how the virtual disk is to be opened.

### -field Version2.ParentVirtualStorageType

A <a href="/windows/win32/api/virtdisk/ns-virtdisk-virtual_storage_type">VIRTUAL_STORAGE_TYPE</a> structure describing 
        the parent virtual disk specified in the <b>ParentPath</b> member.

### -field Version2.SourceVirtualStorageType

A <a href="/windows/win32/api/virtdisk/ns-virtdisk-virtual_storage_type">VIRTUAL_STORAGE_TYPE</a> structure describing 
        the source virtual disk specified in the <b>SourcePath</b> member.

### -field Version2.ResiliencyGuid

Resiliency <b>GUID</b> for the file.

> [!NOTE]
> The following parameters prefaced Version3 and Version4 are intended for internal use.

## -syntax 

```cpp
typedef struct _CREATE_VIRTUAL_DISK_PARAMETERS {
  CREATE_VIRTUAL_DISK_VERSION Version;
  union {
    struct {
      GUID      UniqueId;
      ULONGLONG MaximumSize;
      ULONG     BlockSizeInBytes;
      ULONG     SectorSizeInBytes;
      PCWSTR    ParentPath;
      PCWSTR    SourcePath;
    } Version1;
    struct {
      GUID                   UniqueId;
      ULONGLONG              MaximumSize;
      ULONG                  BlockSizeInBytes;
      ULONG                  SectorSizeInBytes;
      ULONG                  PhysicalSectorSizeInBytes;
      PCWSTR                 ParentPath;
      PCWSTR                 SourcePath;
      OPEN_VIRTUAL_DISK_FLAG OpenFlags;
      VIRTUAL_STORAGE_TYPE   ParentVirtualStorageType;
      VIRTUAL_STORAGE_TYPE   SourceVirtualStorageType;
      GUID                   ResiliencyGuid;
    } Version2;
  };
} CREATE_VIRTUAL_DISK_PARAMETERS, *PCREATE_VIRTUAL_DISK_PARAMETERS;
```

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/windows/win32/api/virtdisk/nf-virtdisk-createvirtualdisk">CreateVirtualDisk</a>



<a href="/windows/desktop/FileIO/naming-a-file">Naming Files, Paths, and Namespaces</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>



<a href="/previous-versions/windows/desktop/legacy/dd323701(v=vs.85)">VHD Structures</a>