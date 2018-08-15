---
UID: NF:virtdisk.GetVirtualDiskInformation
title: GetVirtualDiskInformation function
author: windows-sdk-content
description: Retrieves information about a VHD.
old-location: vhd\getvirtualdiskinformation.htm
old-project: VStor
ms.assetid: c3832be0-e9b8-4f6a-a663-06349c7fd639
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetVirtualDiskInformation, GetVirtualDiskInformation function [VHD], vdssys/GetVirtualDiskInformation, vhd.getvirtualdiskinformation, virtdisk/GetVirtualDiskInformation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: virtdisk.h
req.include-header: 
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - VirtDisk.dll
api_name:
 - GetVirtualDiskInformation
product: Windows
targetos: Windows
req.lib: VirtDisk.lib
req.dll: VirtDisk.dll
req.irql: 
req.product: Windows UI
---

# GetVirtualDiskInformation function


## -description


Retrieves information about a virtual hard disk (VHD).


## -parameters




### -param VirtualDiskHandle [in]

A handle to the open VHD, which must have been opened using the 
      <b>VIRTUAL_DISK_ACCESS_GET_INFO</b> flag set in the 
      <i>VirtualDiskAccessMask</i> parameter to the 
      <a href="https://msdn.microsoft.com/08e2a82d-9110-42b1-be09-dc5150da42f6">OpenVirtualDisk</a> function. For information on how to 
      open a VHD, see the <b>OpenVirtualDisk</b> function.


### -param VirtualDiskInfoSize [in, out]

A pointer to a <b>ULONG</b> that contains the size of the 
      <i>VirtualDiskInfo</i> parameter.


### -param VirtualDiskInfo [in, out]

A pointer to a valid <a href="https://msdn.microsoft.com/666c1d6e-cf23-4452-98ea-e7d4c31c3d3b">GET_VIRTUAL_DISK_INFO</a> 
      structure. The format of the data returned is dependent on the value passed in the 
      <b>Version</b> member by the caller.


### -param SizeUsed [in, out, optional]

A pointer to a <b>ULONG</b> that contains the size used.


## -returns



Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b> and the 
       <i>VirtualDiskInfo</i> parameter contains the requested information.

If the function fails, the return value is an error code and the <i>VirtualDiskInfo</i> 
       parameter is undefined. For more information, see 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



The <b>GetVirtualDiskInformation</b> function 
    can be called on any valid <i>VirtualDiskHandle</i>, provided the handle was opened using the 
    <b>VIRTUAL_DISK_ACCESS_GET_INFO</b> flag. The VHD is not required to be an attached disk.




## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/666c1d6e-cf23-4452-98ea-e7d4c31c3d3b">GET_VIRTUAL_DISK_INFO</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

