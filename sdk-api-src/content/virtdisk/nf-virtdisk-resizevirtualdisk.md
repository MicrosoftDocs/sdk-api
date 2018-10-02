---
UID: NF:virtdisk.ResizeVirtualDisk
title: ResizeVirtualDisk function
author: windows-sdk-content
description: Resizes a virtual disk.
old-location: vstor\resizevirtualdisk.htm
tech.root: VStor
ms.assetid: d000c03e-c0ad-4054-b2eb-1aca34a95816
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ResizeVirtualDisk, ResizeVirtualDisk function [Virtual Storage], virtdisk/ResizeVirtualDisk, vstor.resizevirtualdisk
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: virtdisk.h
req.include-header: Windows.h
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
 - ResizeVirtualDisk
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ResizeVirtualDisk function


## -description


Resizes a virtual disk.


## -parameters




### -param VirtualDiskHandle [in]

Handle to an open virtual disk.


### -param Flags [in]

Zero or more flags enumerated from the 
      <a href="https://msdn.microsoft.com/dd4fc68d-8bed-47ce-94a2-a8a71199fac2">RESIZE_VIRTUAL_DISK_FLAG</a> enumeration.


### -param Parameters [in]

Address of a 
      <a href="https://msdn.microsoft.com/ff44f07a-67d1-4ad3-be2b-0aea1d3c4a6a">RESIZE_VIRTUAL_DISK_PARAMETERS</a> 
      structure containing the new size of the virtual disk.


### -param Overlapped [in, optional]

If this is to be an asynchronous operation, the address of a valid 
      <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure.


## -returns



Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code. For more information, see 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/dd4fc68d-8bed-47ce-94a2-a8a71199fac2">RESIZE_VIRTUAL_DISK_FLAG</a>



<a href="https://msdn.microsoft.com/ff44f07a-67d1-4ad3-be2b-0aea1d3c4a6a">RESIZE_VIRTUAL_DISK_PARAMETERS</a>



<a href="https://msdn.microsoft.com/79c3b3ad-4eaf-49ce-a8ee-b26faf6c2cba">VHD Functions</a>
 

 

