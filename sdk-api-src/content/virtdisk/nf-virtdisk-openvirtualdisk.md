---
UID: NF:virtdisk.OpenVirtualDisk
title: OpenVirtualDisk function
author: windows-driver-content
description: Opens a virtual hard disk (VHD) or CD or DVD image file (ISO) for use.
old-location: vhd\openvirtualdisk.htm
old-project: VStor
ms.assetid: 08e2a82d-9110-42b1-be09-dc5150da42f6
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: OpenVirtualDisk, OpenVirtualDisk function [VHD], vhd.openvirtualdisk, virtdisk/OpenVirtualDisk
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: virtdisk.h
req.include-header: Windows.h
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
req.typenames: VIRTUAL_DISK_ACCESS_MASK, VIRTUAL_DISK_ACCESS_MASK
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	VirtDisk.dll
api_name:
-	OpenVirtualDisk
product: Windows
targetos: Windows
req.lib: VirtDisk.lib
req.dll: VirtDisk.dll
req.irql: 
req.product: Windows UI
---

# OpenVirtualDisk function


## -description


Opens a virtual hard disk (VHD) or CD or DVD image file (ISO) for use.


## -parameters




### -param VirtualStorageType [in]

A pointer to a valid <a href="https://msdn.microsoft.com/9f0c1848-fa8e-4747-a3b1-71a274695280">VIRTUAL_STORAGE_TYPE</a> 
     structure.


### -param Path [in]

A pointer to a valid path to the virtual disk image to open.


### -param VirtualDiskAccessMask [in]

A valid value of the 
     <a href="https://msdn.microsoft.com/2b1f02ab-dc32-4af1-880b-73e7db8602be">VIRTUAL_DISK_ACCESS_MASK</a> enumeration.


### -param Flags [in]

A valid combination of values of the 
     <a href="https://msdn.microsoft.com/edc7d3ad-23a0-4e7a-82d5-8ac4df785f35">OPEN_VIRTUAL_DISK_FLAG</a> enumeration.


### -param Parameters [in, optional]

An optional pointer to a valid 
     <a href="https://msdn.microsoft.com/ad67bc3e-a0fe-4198-9307-819577abef7f">OPEN_VIRTUAL_DISK_PARAMETERS</a> structure. Can 
     be <b>NULL</b>.


### -param Handle [out]

A pointer to the handle object that represents the open virtual disk.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b> (0) and the 
      <i>Handle</i> parameter contains a valid pointer to the new virtual disk object.

If the function fails, the return value is an error code and the value of the <i>Handle</i> 
      parameter is undefined. For more information, see 
      <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



To prevent an open request failure when attempting to open a handle to a permanently attached virtual disk, 
    the following requirements apply: 

<ul>
<li>The <i>VirtualDiskAccessMask</i> parameter must include the 
      <b>VIRTUAL_DISK_ACCESS_DETACH</b> (0x00040000) flag.</li>
<li>Write access to the file must not be requested if the original open operation that created the permanently 
      attached virtual disk only requested read access.</li>
</ul>
If the <b>OpenVirtualDisk</b> function fails with an error 
    code value of <b>ERROR_INVALID_PARAMETER</b> (87), the cause may be due to any of the following 
    conditions:

<ul>
<li>The <i>VirtualStorageType</i> parameter is <b>NULL</b>.</li>
<li>The <i>Path</i> parameter is <b>NULL</b>.</li>
<li>The <i>VirtualDiskAccessMask</i> parameter is set to a value of 
      <code>(VirtualDiskAccessMask &amp; ~VIRTUAL_DISK_ACCESS_ALL)</code>.</li>
<li>The <i>Flags</i> parameter is set to a value of 
      <code>(Flags &amp; ~(OPEN_VIRTUAL_DISK_FLAG_NO_PARENTS | OPEN_VIRTUAL_DISK_FLAG_BLANK_FILE))</code>.</li>
<li>The <b>Version</b> member of the <i>Parameters</i> parameter is not 
      set to <b>OPEN_VIRTUAL_DISK_VERSION_1</b>.</li>
</ul>
The host volume that contains the virtual disk image file cannot be compressed or EFS encrypted. This function 
    will fail with error <b>ERROR_UNSUPPORTED_COMPRESSION</b> (618) if the host volume has been 
    compressed or with error <b>ERROR_FILE_ENCRYPTED</b> (6002) if the host volume has been EFS 
    encrypted after the initial virtual disk creation.

The path pointed to by the <i>Path</i> parameter cannot be on a local network share (that 
    is a network share via loopback). This function will fail with error 
    <b>ERROR_FILE_SYSTEM_LIMITATION</b> (665) if the path is on a local network share. This 
    function will fail with error <b>ERROR_FILE_CORRUPT</b> (1392) if an ISO virtual disk is being 
    opened and the file size is not an even multiple of 2 KB (2,048 bytes), is at least 34 KB (34,816 bytes), or the 
    volume structure descriptor does not contain a known CDFS or UDFS volume identifier.

When an application is finished using the object handle returned in the <i>Handle</i> 
    parameter, use the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function to close the 
    handle.

CD and DVD image files (ISO) are not supported before Windows 8 and 
    Windows Server 2012.




## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/9d9f187e-dea1-48ca-a3fe-9e9c513e9088">CreateVirtualDisk</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

