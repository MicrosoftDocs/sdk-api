---
UID: NF:virtdisk.CreateVirtualDisk
title: CreateVirtualDisk function (virtdisk.h)
description: Creates a virtual hard disk (VHD) image file, either using default parameters or using an existing virtual disk or physical disk.
helpviewer_keywords: ["CreateVirtualDisk","CreateVirtualDisk function [VHD]","vdssys/CreateVirtualDisk","vhd.createvirtualdisk","virtdisk/CreateVirtualDisk"]
old-location: vhd\createvirtualdisk.htm
tech.root: VStor
ms.assetid: 9d9f187e-dea1-48ca-a3fe-9e9c513e9088
ms.date: 12/05/2018
ms.keywords: CreateVirtualDisk, CreateVirtualDisk function [VHD], vdssys/CreateVirtualDisk, vhd.createvirtualdisk, virtdisk/CreateVirtualDisk
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
req.lib: VirtDisk.lib
req.dll: VirtDisk.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateVirtualDisk
 - virtdisk/CreateVirtualDisk
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - VirtDisk.dll
api_name:
 - CreateVirtualDisk
---

# CreateVirtualDisk function


## -description

Creates a virtual hard disk (VHD) image file, either using default parameters or using an existing 
    virtual disk or physical disk.

## -parameters

### -param VirtualStorageType [in]

A pointer to a <a href="/windows/win32/api/virtdisk/ns-virtdisk-virtual_storage_type">VIRTUAL_STORAGE_TYPE</a> structure 
     that contains the desired disk type and vendor information.

### -param Path [in]

A pointer to a valid string that represents the path to the new virtual disk image file.

### -param VirtualDiskAccessMask [in]

The <a href="/windows/win32/api/virtdisk/ne-virtdisk-virtual_disk_access_mask-r1">VIRTUAL_DISK_ACCESS_MASK</a> value to use 
     when opening the newly created virtual disk file. If the <b>Version</b> member of the 
     <i>Parameters</i> parameter is set to 
     <b>CREATE_VIRTUAL_DISK_VERSION_2</b> then only the 
     <b>VIRTUAL_DISK_ACCESS_NONE</b> (0) value may be specified.

### -param SecurityDescriptor [in, optional]

An optional pointer to a 
     <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor">SECURITY_DESCRIPTOR</a> to apply to the virtual 
     disk image file. If this parameter is <b>NULL</b>, the parent directory's security descriptor 
     will be used.

### -param Flags [in]

Creation flags, which must be a valid combination of the 
     <a href="/windows/win32/api/virtdisk/ne-virtdisk-create_virtual_disk_flag">CREATE_VIRTUAL_DISK_FLAG</a> enumeration.

### -param ProviderSpecificFlags [in]

Flags specific to the type of virtual disk being created. May be zero if none are required.

### -param Parameters [in]

A pointer to a valid 
     <a href="/windows/win32/api/virtdisk/ns-virtdisk-create_virtual_disk_parameters">CREATE_VIRTUAL_DISK_PARAMETERS</a> structure 
     that contains creation parameter data.

### -param Overlapped [in, optional]

An optional pointer to a valid <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure 
     if <a href="/windows/desktop/Sync/synchronization-and-overlapped-input-and-output">asynchronous</a> operation 
     is desired.

### -param Handle [out]

A pointer to the handle object that represents the newly created virtual disk.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b> and the 
      <i>Handle</i> parameter contains a valid pointer to the new virtual disk object.

If the function fails, the return value is an error code and the value of the <i>Handle</i> 
      parameter is undefined. For more information, see 
      <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

If the <b>CreateVirtualDisk</b> function fails with an 
    error code value of <b>ERROR_INVALID_PARAMETER</b>, the cause may be due to any of the 
    following conditions:

<ul>
<li>The <i>VirtualStorageType</i> parameter is <b>NULL</b>.</li>
<li>The <i>Parameters</i> parameter is <b>NULL</b>.</li>
<li>The <b>Version</b> member of the <i>Parameters</i> parameter is not 
      set to <b>CREATE_VIRTUAL_DISK_VERSION_1</b> or 
      <b>CREATE_VIRTUAL_DISK_VERSION_2</b>.</li>
<li>The <b>Version</b> member of the <i>Parameters</i> parameter is set 
      to <b>CREATE_VIRTUAL_DISK_VERSION_2</b> but the 
      <i>VirtualDiskAccessMask</i> parameter is not set to 
      <b>VIRTUAL_DISK_ACCESS_NONE</b>.</li>
<li>The <b>BlockSizeInBytes</b> member of the  <i>Parameters</i> 
      parameter is not set to  <b>CREATE_VIRTUAL_DISK_PARAMETERS_DEFAULT_BLOCK_SIZE</b> (0), 
      0x80000 (512 KB), or 0x200000 (2 MB).</li>
<li>The <b>MaximumSize</b> member of the <i>Parameters</i> parameter is 
      less than 3 MB.</li>
<li>The <b>MaximumSize</b> member of the <i>Parameters</i> parameter is 
      not aligned with the value of the <b>SectorSizeInBytes</b> member.</li>
<li>The <i>VirtualDiskAccessMask</i> parameter is set to a value of 
      <code>(VirtualDiskAccessMask &amp; ~VIRTUAL_DISK_ACCESS_ALL)</code>.</li>
<li>The <i>Flags</i> parameter is larger than 
      <b>CREATE_VIRTUAL_DISK_FLAG_FULL_PHYSICAL_ALLOCATION</b>.</li>
</ul>
The host volume containing the new virtual disk image file cannot be compressed or EFS encrypted.

When creating the various types of virtual disks, the following combinations of creation parameters are 
      recommended:

<ul>
<li>The <b>CREATE_VIRTUAL_DISK_FLAG_FULL_PHYSICAL_ALLOCATION</b> flag should be 
        specified.</li>
<li><b>ParentPath</b> should not be specified.</li>
<li><b>SourcePath</b> can be specified if desired.</li>
</ul>
<ul>
<li>The <b>CREATE_VIRTUAL_DISK_FLAG_FULL_PHYSICAL_ALLOCATION</b> flag should not be 
        specified.</li>
<li><b>ParentPath</b> should not be specified.</li>
<li><b>SourcePath</b> can be specified if desired.</li>
</ul>
<ul>
<li>The <b>CREATE_VIRTUAL_DISK_FLAG_FULL_PHYSICAL_ALLOCATION</b> flag should not be 
        specified.</li>
<li><b>ParentPath</b> should be specified.</li>
<li><b>SourcePath</b> should not be specified.</li>
</ul>
The <b>CreateVirtualDisk</b> function can also be used 
    as a mechanism for converting one type of virtual disk to another, or a physical disk to a virtual disk. This is 
    accomplished through the use of the <b>SourcePath</b> member of the 
    <a href="/windows/win32/api/virtdisk/ns-virtdisk-create_virtual_disk_parameters">CREATE_VIRTUAL_DISK_PARAMETERS</a> structure 
    to pre-populate the new virtual disk with block data from the source disk.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk">OpenVirtualDisk</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>