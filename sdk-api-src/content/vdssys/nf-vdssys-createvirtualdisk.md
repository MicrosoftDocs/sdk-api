---
UID: NF:vdssys.CreateVirtualDisk
title: CreateVirtualDisk function
author: windows-sdk-content
description: Creates a virtual hard disk (VHD) image file, either using default parameters or using an existing virtual disk or physical disk.
old-location: vhd\createvirtualdisk.htm
old-project: VStor
ms.assetid: 9d9f187e-dea1-48ca-a3fe-9e9c513e9088
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: CreateVirtualDisk, CreateVirtualDisk function [VHD], vdssys/CreateVirtualDisk, vhd.createvirtualdisk, virtdisk/CreateVirtualDisk
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: vdssys.h
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
req.typenames: VIRTUAL_DISK_ACCESS_MASK
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	VirtDisk.dll
api_name:
-	CreateVirtualDisk
product: Windows
targetos: Windows
req.lib: VirtDisk.lib
req.dll: VirtDisk.dll
req.irql: 
req.product: Windows UI
---

# CreateVirtualDisk function


## -description


Creates a virtual hard disk (VHD) image file, either using default parameters or using an existing 
    virtual disk or physical disk.


## -parameters




### -param VirtualStorageType [in]

A pointer to a <a href="https://msdn.microsoft.com/9f0c1848-fa8e-4747-a3b1-71a274695280">VIRTUAL_STORAGE_TYPE</a> structure 
     that contains the desired disk type and vendor information.


### -param Path [in]

A pointer to a valid string that represents the path to the new virtual disk image file.


### -param VirtualDiskAccessMask [in]

The <a href="https://msdn.microsoft.com/2b1f02ab-dc32-4af1-880b-73e7db8602be">VIRTUAL_DISK_ACCESS_MASK</a> value to use 
     when opening the newly created virtual disk file. If the <b>Version</b> member of the 
     <i>Parameters</i> parameter is set to 
     <b>CREATE_VIRTUAL_DISK_VERSION_2</b> then only the 
     <b>VIRTUAL_DISK_ACCESS_NONE</b> (0) value may be specified.


### -param SecurityDescriptor [in, optional]

An optional pointer to a 
     <a href="https://msdn.microsoft.com/library/windows/hardware/ff563689">SECURITY_DESCRIPTOR</a> to apply to the virtual 
     disk image file. If this parameter is <b>NULL</b>, the parent directory's security descriptor 
     will be used.


### -param Flags [in]

Creation flags, which must be a valid combination of the 
     <a href="https://msdn.microsoft.com/35dba6c6-2825-425a-b432-a6ac8ad4ea4b">CREATE_VIRTUAL_DISK_FLAG</a> enumeration.


### -param ProviderSpecificFlags [in]

Flags specific to the type of virtual disk being created. May be zero if none are required.


### -param Parameters [in]

A pointer to a valid 
     <a href="https://msdn.microsoft.com/797e21ae-a4c4-48df-8124-e5c2fad22f33">CREATE_VIRTUAL_DISK_PARAMETERS</a> structure 
     that contains creation parameter data.


### -param Overlapped [in, optional]

An optional pointer to a valid <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure 
     if <a href="https://msdn.microsoft.com/db44990e-5a0f-4153-8ff6-79dd7cda48af">asynchronous</a> operation 
     is desired.


### -param Handle [out]

A pointer to the handle object that represents the newly created virtual disk.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b> and the 
      <i>Handle</i> parameter contains a valid pointer to the new virtual disk object.

If the function fails, the return value is an error code and the value of the <i>Handle</i> 
      parameter is undefined. For more information, see 
      <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




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
    <a href="https://msdn.microsoft.com/797e21ae-a4c4-48df-8124-e5c2fad22f33">CREATE_VIRTUAL_DISK_PARAMETERS</a> structure 
    to pre-populate the new virtual disk with block data from the source disk.




## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/08e2a82d-9110-42b1-be09-dc5150da42f6">OpenVirtualDisk</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

