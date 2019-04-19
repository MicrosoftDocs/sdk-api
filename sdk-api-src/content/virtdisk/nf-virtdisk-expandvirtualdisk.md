---
UID: NF:virtdisk.ExpandVirtualDisk
title: ExpandVirtualDisk function (virtdisk.h)
author: windows-sdk-content
description: Increases the size of a fixed or dynamically expandable virtual hard disk (VHD).
old-location: vhd\expandvirtualdisk.htm
tech.root: VStor
ms.assetid: 96d1b603-c019-4868-9b81-3a5628fbb50c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ExpandVirtualDisk, ExpandVirtualDisk function [VHD], vdssys/ExpandVirtualDisk, vhd.expandvirtualdisk, virtdisk/ExpandVirtualDisk
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
 - ExpandVirtualDisk
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ExpandVirtualDisk function


## -description


Increases the size of a fixed or dynamically expandable virtual hard disk (VHD).


## -parameters




### -param VirtualDiskHandle [in]

A handle to the open virtual disk, which must have been opened using the <b>VIRTUAL_DISK_ACCESS_METAOPS</b> flag. For information on how to open a virtual disk, see the <a href="https://msdn.microsoft.com/en-us/library/Dd323680(v=VS.85).aspx">OpenVirtualDisk</a> function.


### -param Flags [in]

Must be the <b>EXPAND_VIRTUAL_DISK_FLAG_NONE</b> value of the <a href="https://msdn.microsoft.com/en-us/library/Dd323665(v=VS.85).aspx">EXPAND_VIRTUAL_DISK_FLAG</a> enumeration.


### -param Parameters [in]

A pointer to a valid <a href="https://msdn.microsoft.com/en-us/library/Dd323667(v=VS.85).aspx">EXPAND_VIRTUAL_DISK_PARAMETERS</a> structure that contains expansion parameter data.


### -param Overlapped [in, optional]

An optional pointer to a valid <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure if <a href="https://msdn.microsoft.com/db44990e-5a0f-4153-8ff6-79dd7cda48af">asynchronous</a> operation is desired.


## -returns



Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code. For more information, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



The <b>ExpandVirtualDisk</b> function performs the operation in-place, and therefore does not create a virtual disk.

The expand operation is valid only for fixed and expandable virtual disks and will invalidate a differencing virtual disk chain.

Expanding a virtual disk requires that the virtual disk be detached during the operation.

The caller must have READ|WRITE access to the backing store for the virtual disk.

For an expandable virtual disk, the <b>ExpandVirtualDisk</b> function may not result in a larger file because the size is virtual and would not actually grow physically until used.

If the virtual disk is expandable and the host volume does not have enough space for the new size, the <b>ExpandVirtualDisk</b> function can succeed anyway. Future writes to the virtual disk may fail if the host volume runs out of space as the virtual disk expands.




## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

