---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# GetStorageDependencyInformation function


## -description


Returns the relationships between virtual hard disks (VHDs) or CD or DVD image file (ISO) or the 
    volumes contained within those disks and their parent disk or volume.


## -parameters




### -param ObjectHandle [in]

A handle to a volume or root directory if  the <i>Flags</i> parameter does not specify 
      the <b>GET_STORAGE_DEPENDENCY_FLAG_DISK_HANDLE</b> flag. For information on how to open a 
      volume or root directory, see the <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function.

If the <i>Flags</i> parameter specifies the 
      <b>GET_STORAGE_DEPENDENCY_FLAG_DISK_HANDLE</b> flag, this handle should be a handle to a 
      disk.


### -param Flags [in]

A valid combination of 
     <a href="https://msdn.microsoft.com/6a438edf-698b-4b2d-8864-c97fbf9eaa9f">GET_STORAGE_DEPENDENCY_FLAG</a> values.


### -param StorageDependencyInfoSize [in]

Size, in bytes, of the buffer that the <i>StorageDependencyInfo</i> parameter refers 
     to.


### -param StorageDependencyInfo [in, out]

A pointer to a buffer to receive the populated 
     <a href="https://msdn.microsoft.com/67648a4d-3f66-407e-9036-c7072bc7e460">STORAGE_DEPENDENCY_INFO</a> structure, which is a 
     variable-length structure.


### -param SizeUsed [in, out, optional]

An optional pointer to a <b>ULONG</b> that receives the size used.


## -returns



Status of the request.

If the function succeeds, the return value is <b>ERROR_SUCCESS</b> and the 
      <i>StorageDependencyInfo</i> parameter contains the requested dependency information.

If the function fails, the return value is an error code and the 
      <i>StorageDependencyInfo</i> parameter is undefined. For more information, see 
      <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



CD and DVD image files (ISO) are not supported before Windows 8 and 
    Windows Server 2012.




## -see-also




<a href="https://msdn.microsoft.com/c9531c07-ad55-42b6-8685-7f55a47e8485">About VHD</a>



<a href="https://msdn.microsoft.com/3b5d0da0-2b23-4b7c-b007-ed3fe030926c">VHD Reference</a>
 

 

