---
UID: NF:virtdisk.DeleteVirtualDiskMetadata
title: DeleteVirtualDiskMetadata function (virtdisk.h)
author: windows-sdk-content
description: Deletes metadata from a virtual disk.
old-location: vstor\deletevirtualdiskmetadata.htm
tech.root: VStor
ms.assetid: 16fbb793-84a9-4dac-a85e-0f4f50ae8e35
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DeleteVirtualDiskMetadata, DeleteVirtualDiskMetadata function [Virtual Storage], virtdisk/DeleteVirtualDiskMetadata, vstor.deletevirtualdiskmetadata
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
 - DeleteVirtualDiskMetadata
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DeleteVirtualDiskMetadata function


## -description


Deletes metadata from a virtual disk.


## -parameters




### -param VirtualDiskHandle [in]

A handle to the open virtual disk.


### -param Item [in]

The item to be deleted.


## -returns



Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is an error code. For more information, see 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/79c3b3ad-4eaf-49ce-a8ee-b26faf6c2cba">VHD Functions</a>
 

 

