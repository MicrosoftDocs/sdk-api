---
UID: NF:virtdisk.BreakMirrorVirtualDisk
title: BreakMirrorVirtualDisk function
author: windows-sdk-content
description: Breaks a previously initiated mirror operation and sets the mirror to be the active virtual disk.
old-location: vhd\breakmirrorvirtualdisk.htm
old-project: VStor
ms.assetid: bf70ee43-9fba-4856-a1bc-85eec61f5763
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: BreakMirrorVirtualDisk, BreakMirrorVirtualDisk function [VHD], vdssys/BreakMirrorVirtualDisk, vhd.breakmirrorvirtualdisk, virtdisk/BreakMirrorVirtualDisk
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: virtdisk.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - VirtDisk.dll
api_name:
 - BreakMirrorVirtualDisk
product: Windows
targetos: Windows
req.lib: VirtDisk.lib
req.dll: VirtDisk.dll
req.irql: 
req.product: Windows UI
---

# BreakMirrorVirtualDisk function


## -description


Breaks a previously initiated mirror operation and sets the mirror to be the active virtual 
    disk.


## -parameters




### -param VirtualDiskHandle [in]

A handle to the open mirrored virtual disk. For information on how to open a virtual disk, see the 
      <a href="https://msdn.microsoft.com/08e2a82d-9110-42b1-be09-dc5150da42f6">OpenVirtualDisk</a> function. For information on how to 
      mirror a virtual disk, see the <a href="https://msdn.microsoft.com/eb72043a-7515-42c0-900d-feed4503ea7a">MirrorVirtualDisk</a> 
      function.


## -returns



Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code. For more information, see 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/eb72043a-7515-42c0-900d-feed4503ea7a">MirrorVirtualDisk</a>



<a href="https://msdn.microsoft.com/08e2a82d-9110-42b1-be09-dc5150da42f6">OpenVirtualDisk</a>



<a href="https://msdn.microsoft.com/79c3b3ad-4eaf-49ce-a8ee-b26faf6c2cba">VHD Functions</a>
 

 

