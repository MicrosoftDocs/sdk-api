---
UID: NF:virtdisk.GetVirtualDiskPhysicalPath
title: GetVirtualDiskPhysicalPath function (virtdisk.h)
description: Retrieves the path to the physical device object that contains a virtual hard disk (VHD) or CD or DVD image file (ISO).
helpviewer_keywords: ["GetVirtualDiskPhysicalPath","GetVirtualDiskPhysicalPath function [VHD]","vdssys/GetVirtualDiskPhysicalPath","vhd.getvirtualdiskphysicalpath","virtdisk/GetVirtualDiskPhysicalPath"]
old-location: vhd\getvirtualdiskphysicalpath.htm
tech.root: VStor
ms.assetid: e17d9b37-c0fc-4513-a224-a918e679707d
ms.date: 12/05/2018
ms.keywords: GetVirtualDiskPhysicalPath, GetVirtualDiskPhysicalPath function [VHD], vdssys/GetVirtualDiskPhysicalPath, vhd.getvirtualdiskphysicalpath, virtdisk/GetVirtualDiskPhysicalPath
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
 - GetVirtualDiskPhysicalPath
 - virtdisk/GetVirtualDiskPhysicalPath
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
 - GetVirtualDiskPhysicalPath
---

# GetVirtualDiskPhysicalPath function


## -description

Retrieves the path to the physical device object that contains a virtual hard disk 
    (VHD) or CD or DVD image file (ISO).

## -parameters

### -param VirtualDiskHandle [in]

A handle to the open virtual disk, which must have been opened using the 
     <b>VIRTUAL_DISK_ACCESS_GET_INFO</b> flag. For information on how to open a virtual disk, see 
     the <a href="/windows/win32/api/virtdisk/nf-virtdisk-openvirtualdisk">OpenVirtualDisk</a> function.

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
      <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

For the <b>GetVirtualDiskPhysicalPath</b> 
    function to succeed, the virtual disk referred to by the <i>VirtualDiskHandle</i> parameter 
    must be attached, the physical disk object must be to be located by the system, and the 
    <i>DiskPath</i> parameter must refer to a buffer large enough to hold the resulting path. This 
    path is in the form &#92;&#92;.&#92;<i>PhysicalDriveX</i> where <i>X</i> 
    is an integer that represents the particular enumeration of the physical disk on the caller's system.

CD and DVD image files (ISO) are not supported before Windows 8 and 
    Windows Server 2012.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>