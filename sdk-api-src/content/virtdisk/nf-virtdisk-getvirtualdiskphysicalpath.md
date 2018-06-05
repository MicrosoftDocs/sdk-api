---
UID: NF:virtdisk.GetVirtualDiskPhysicalPath
title: GetVirtualDiskPhysicalPath function
author: windows-sdk-content
description: Retrieves the path to the physical device object that contains a virtual hard disk (VHD) or CD or DVD image file (ISO).
old-location: vhd\getvirtualdiskphysicalpath.htm
old-project: VStor
ms.assetid: e17d9b37-c0fc-4513-a224-a918e679707d
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetVirtualDiskPhysicalPath, GetVirtualDiskPhysicalPath function [VHD], vdssys/GetVirtualDiskPhysicalPath, vhd.getvirtualdiskphysicalpath, virtdisk/GetVirtualDiskPhysicalPath
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: VIRTUAL_DISK_ACCESS_MASK
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	VirtDisk.dll
api_name:
-	GetVirtualDiskPhysicalPath
product: Windows
targetos: Windows
req.lib: VirtDisk.lib
req.dll: VirtDisk.dll
req.irql: 
req.product: Windows UI
---

# GetVirtualDiskPhysicalPath function


## -description


Retrieves the path to the physical device object that contains a virtual hard disk 
    (VHD) or CD or DVD image file (ISO).


## -parameters




### -param VirtualDiskHandle [in]

A handle to the open virtual disk, which must have been opened using the 
     <b>VIRTUAL_DISK_ACCESS_GET_INFO</b> flag. For information on how to open a virtual disk, see 
     the <a href="https://msdn.microsoft.com/08e2a82d-9110-42b1-be09-dc5150da42f6">OpenVirtualDisk</a> function.


### -param DiskPathSizeInBytes [in, out]

The size, in bytes, of the buffer pointed to by the <i>DiskPath</i> parameter.


### -param DiskPath [out, optional]

A target buffer to receive the path of the physical disk device that contains the virtual disk.


## -returns



Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b> and the 
      <i>DiskPath</i> parameter contains a pointer to a populated string.

If the function fails, the return value is an error code and the value of the contents of the buffer referred 
      to by the  <i>DiskPath</i> parameter is undefined. For more information, see 
      <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



For the <b>GetVirtualDiskPhysicalPath</b> 
    function to succeed, the virtual disk referred to by the <i>VirtualDiskHandle</i> parameter 
    must be attached, the physical disk object must be to be located by the system, and the 
    <i>DiskPath</i> parameter must refer to a buffer large enough to hold the resulting path. This 
    path is in the form \\.\<i>PhysicalDriveX</i> where <i>X</i> 
    is an integer that represents the particular enumeration of the physical disk on the caller's system.

CD and DVD image files (ISO) are not supported before Windows 8 and 
    Windows Server 2012.




## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

