---
UID: NS:winioctl._FILE_ALLOCATED_RANGE_BUFFER
title: FILE_ALLOCATED_RANGE_BUFFER
author: windows-sdk-content
description: Indicates a range of bytes in a file.
old-location: fs\file_allocated_range_buffer_str.htm
tech.root: FileIO
ms.assetid: e9c7d757-df29-4419-baba-56beb41623bf
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PFILE_ALLOCATED_RANGE_BUFFER, FILE_ALLOCATED_RANGE_BUFFER, FILE_ALLOCATED_RANGE_BUFFER structure [Files], PFILE_ALLOCATED_RANGE_BUFFER, PFILE_ALLOCATED_RANGE_BUFFER structure pointer [Files], _win32_file_allocated_range_buffer_str, base.file_allocated_range_buffer_str, fs.file_allocated_range_buffer_str, winioctl/FILE_ALLOCATED_RANGE_BUFFER, winioctl/PFILE_ALLOCATED_RANGE_BUFFER"
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinIoCtl.h
api_name:
 - FILE_ALLOCATED_RANGE_BUFFER
product: Windows
targetos: Windows
req.typenames: FILE_ALLOCATED_RANGE_BUFFER, *PFILE_ALLOCATED_RANGE_BUFFER
req.redist: 
---

# FILE_ALLOCATED_RANGE_BUFFER structure


## -description


Indicates a range of bytes in a file. This structure is used with the 
<a href="https://msdn.microsoft.com/053e26ec-1529-41b3-aeb6-128b3085bafc">FSCTL_QUERY_ALLOCATED_RANGES</a> control code. On input, the structure indicates the range of the file to search. On output, the operation retrieves an array of 
<b>FILE_ALLOCATED_RANGE_BUFFER</b> structures to indicate the allocated ranges within the search range.


## -struct-fields




### -field FileOffset

The file offset of the start of a range of bytes in a file, in bytes.


### -field Length

The size of the range, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/053e26ec-1529-41b3-aeb6-128b3085bafc">FSCTL_QUERY_ALLOCATED_RANGES</a>



<a href="https://msdn.microsoft.com/7326041d-f11e-4b80-ac4e-07173e418ce7">Sparse Files</a>
 

 

