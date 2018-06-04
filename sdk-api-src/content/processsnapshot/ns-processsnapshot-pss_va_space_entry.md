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

# PSS_VA_SPACE_ENTRY structure


## -description


Holds the <a href="https://msdn.microsoft.com/library/windows/hardware/dn957515">MEMORY_BASIC_INFORMATION</a> returned by <a href="https://msdn.microsoft.com/C6AC38B5-0A1C-44D7-A1F6-8196AE9B8FB0">PssWalkSnapshot</a> for a virtual address (VA) region.


## -struct-fields




### -field BaseAddress

Information about the VA region. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn957515">MEMORY_BASIC_INFORMATION</a>.


### -field AllocationBase

Information about the VA region. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn957515">MEMORY_BASIC_INFORMATION</a>.


### -field AllocationProtect

Information about the VA region. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn957515">MEMORY_BASIC_INFORMATION</a>.


### -field RegionSize

Information about the VA region. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn957515">MEMORY_BASIC_INFORMATION</a>.


### -field State

Information about the VA region. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn957515">MEMORY_BASIC_INFORMATION</a>.


### -field Protect

Information about the VA region. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn957515">MEMORY_BASIC_INFORMATION</a>.


### -field Type

Information about the VA region. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn957515">MEMORY_BASIC_INFORMATION</a>.


### -field TimeDateStamp

If section information was captured and the region is an executable image (<b>MEM_IMAGE</b>), this is the <b>TimeDateStamp</b> value from the Portable Executable (PE) header which describes the image. It is the low 32 bits of the number of seconds since 00:00 January 1, 1970 (a C run-time time_t value), that indicates when the file was created.


### -field SizeOfImage

If section information was captured and the region is an executable image (<b>MEM_IMAGE</b>), this is the <b>SizeOfImage</b> value from the Portable Executable (PE) header which describes the image. It is the size (in bytes) of the image, including all headers, as the image is loaded in memory.


### -field ImageBase

If section information was captured and the region is an executable image (<b>MEM_IMAGE</b>), this is the <b>ImageBase</b> value from the Portable Executable (PE) header which describes the image. It is the  preferred address of the first byte of the image when loaded into memory.


### -field CheckSum

If section information was captured and the region is an executable image (<b>MEM_IMAGE</b>), this is the <b>CheckSum</b> value from the Portable Executable (PE) header which describes the image. It is the image file checksum. 


### -field MappedFileNameLength

The length of the mapped file name buffer, in bytes.


### -field MappedFileName

If section information was captured, this is the file path backing the section (if any). The path may be in NT namespace. The string may not be terminated by a <b>NULL</b> character. The pointer is valid for the lifetime of the walk marker passed to <a href="https://msdn.microsoft.com/C6AC38B5-0A1C-44D7-A1F6-8196AE9B8FB0">PssWalkSnapshot</a>.


## -remarks




<a href="https://msdn.microsoft.com/C6AC38B5-0A1C-44D7-A1F6-8196AE9B8FB0">PssWalkSnapshot</a> returns a <b>PSS_VA_SPACE_ENTRY</b> structure when the  <a href="https://msdn.microsoft.com/93A79F7F-2164-4F7A-ADE7-C1655EEFC9BF">PSS_WALK_INFORMATION_CLASS</a> member that the caller provides it is <b>PSS_WALK_VA_SPACE</b>.




## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

