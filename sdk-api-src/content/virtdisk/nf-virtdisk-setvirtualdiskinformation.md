---
UID: NF:virtdisk.SetVirtualDiskInformation
title: SetVirtualDiskInformation function (virtdisk.h)
author: windows-sdk-content
description: Sets information about a virtual hard disk (VHD).
old-location: vhd\setvirtualdiskinformation.htm
tech.root: VStor
ms.assetid: bd4bee14-6812-4a28-8c44-2b8e8d42e697
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetVirtualDiskInformation, SetVirtualDiskInformation function [VHD], vdssys/SetVirtualDiskInformation, vhd.setvirtualdiskinformation, virtdisk/SetVirtualDiskInformation
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
req.lib: VirtDisk.lib
req.dll: VirtDisk.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - VirtDisk.dll
api_name:
 - SetVirtualDiskInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetVirtualDiskInformation function


## -description


Sets information about a virtual hard disk (VHD).


## -parameters




### -param VirtualDiskHandle [in]

A handle to the open virtual disk, which must have been opened using the 
     <b>VIRTUAL_DISK_ACCESS_METAOPS</b> flag. For information on how to open a virtual disk, see 
     the <a href="https://docs.microsoft.com/windows/desktop/api/vdssys/nf-vdssys-openvirtualdisk">OpenVirtualDisk</a> function.


### -param VirtualDiskInfo [in]

A pointer to a valid <a href="https://docs.microsoft.com/windows/desktop/api/vdssys/ns-vdssys-_set_virtual_disk_info">SET_VIRTUAL_DISK_INFO</a> 
     structure.


## -returns



Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code. For more information, see 
      <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">System Error Codes</a>.




## -remarks



The <b>SetVirtualDiskInformation</b> function 
    will fail if the <b>ParentFilePath</b> member is requested to be set but the system cannot 
    resolve the path provided.

Setting the parent information will also cause the child's parent 
    <b>GUID</b> and Timestamp fields to be updated.

The virtual disk cannot be attached while this operation is in progress.

The caller must have READ|WRITE access to the backing store for the virtual disk.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd323654(v=vs.85)">About VHD</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd323700(v=vs.85)">VHD Reference</a>
 

 

