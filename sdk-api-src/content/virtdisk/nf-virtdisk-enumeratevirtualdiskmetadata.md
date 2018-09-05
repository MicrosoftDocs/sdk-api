---
UID: NF:virtdisk.EnumerateVirtualDiskMetadata
title: EnumerateVirtualDiskMetadata function
author: windows-sdk-content
description: Enumerates the metadata associated with a virtual disk.
old-location: vstor\enumeratevirtualdiskmetadata.htm
old-project: VStor
ms.assetid: 7817863a-38ca-4686-9d66-71700dba852f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EnumerateVirtualDiskMetadata, EnumerateVirtualDiskMetadata function [Virtual Storage], virtdisk/EnumerateVirtualDiskMetadata, vstor.enumeratevirtualdiskmetadata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: virtdisk.h
req.include-header: Windows.h
req.redist: 
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
 - EnumerateVirtualDiskMetadata
product: Windows
targetos: Windows
req.lib: VirtDisk.lib
req.dll: VirtDisk.dll
req.irql: 
req.product: Windows UI
---

# EnumerateVirtualDiskMetadata function


## -description


Enumerates the metadata associated with a virtual disk.


## -parameters




### -param VirtualDiskHandle [in]

Handle to an open virtual disk.


### -param NumberOfItems [in, out]

Address of a <b>ULONG</b>. On input, the value indicates the number of elements in 
      the buffer pointed to by the <i>Items</i> parameter. On output, the value contains the number 
      of items retrieved. If the buffer was too small, the API will fail and return 
      <b>ERROR_INSUFFICIENT_BUFFER</b> and the <b>ULONG</b> will contain the 
      required buffer size.


### -param Items [out]

Address of a buffer to be filled with the <b>GUID</b>s representing the metadata. The 
      <a href="https://msdn.microsoft.com/5dc5cf6e-c218-4aca-a574-499441bd1c12">GetVirtualDiskMetadata</a> function can be used 
      to retrieve the data represented by each <b>GUID</b>.


## -returns



Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the buffer pointed to by the <i>Items</i> parameter was too small, the return value is 
       <b>ERROR_INSUFFICIENT_BUFFER</b>.

If the function fails, the return value is an error code. For more information, see 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/79c3b3ad-4eaf-49ce-a8ee-b26faf6c2cba">VHD Functions</a>
 

 

