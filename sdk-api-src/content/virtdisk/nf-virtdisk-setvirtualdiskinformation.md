---
UID: NF:virtdisk.SetVirtualDiskInformation
title: SetVirtualDiskInformation function
author: windows-sdk-content
description: Sets information about a virtual hard disk (VHD).
old-location: vhd\setvirtualdiskinformation.htm
tech.root: VStor
ms.assetid: bd4bee14-6812-4a28-8c44-2b8e8d42e697
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: SetVirtualDiskInformation, SetVirtualDiskInformation function [VHD], vdssys/SetVirtualDiskInformation, vhd.setvirtualdiskinformation, virtdisk/SetVirtualDiskInformation
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# SetVirtualDiskInformation function


## -description


Sets information about a virtual hard disk (VHD).


## -parameters




### -param VirtualDiskHandle [in]

A handle to the open virtual disk, which must have been opened using the 
     <b>VIRTUAL_DISK_ACCESS_METAOPS</b> flag. For information on how to open a virtual disk, see 
     the <a href="https://msdn.microsoft.com/08e2a82d-9110-42b1-be09-dc5150da42f6">OpenVirtualDisk</a> function.


### -param VirtualDiskInfo [in]

A pointer to a valid <a href="https://msdn.microsoft.com/04b2bb75-7905-469a-abf1-15591dc64686">SET_VIRTUAL_DISK_INFO</a> 
     structure.


## -returns



Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code. For more information, see 
      <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



The <b>SetVirtualDiskInformation</b> function 
    will fail if the <b>ParentFilePath</b> member is requested to be set but the system cannot 
    resolve the path provided.

Setting the parent information will also cause the child's parent 
    <b>GUID</b> and Timestamp fields to be updated.

The virtual disk cannot be attached while this operation is in progress.

The caller must have READ|WRITE access to the backing store for the virtual disk.




## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

