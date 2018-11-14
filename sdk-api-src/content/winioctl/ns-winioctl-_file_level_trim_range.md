---
UID: NS:winioctl._FILE_LEVEL_TRIM_RANGE
title: "_FILE_LEVEL_TRIM_RANGE"
author: windows-sdk-content
description: Specifies a range of a file that is to be trimmed.
old-location: fs\file_level_trim_range.htm
tech.root: fileio
ms.assetid: 2ee14239-68bb-40f6-b10b-2500d316dcc8
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*PFILE_LEVEL_TRIM_RANGE, FILE_LEVEL_TRIM_RANGE, FILE_LEVEL_TRIM_RANGE structure [Files], PFILE_LEVEL_TRIM_RANGE, PFILE_LEVEL_TRIM_RANGE structure pointer [Files], _FILE_LEVEL_TRIM_RANGE, fs.file_level_trim_range, winioctl/FILE_LEVEL_TRIM_RANGE, winioctl/PFILE_LEVEL_TRIM_RANGE"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - FILE_LEVEL_TRIM_RANGE
product: Windows
targetos: Windows
req.typenames: FILE_LEVEL_TRIM_RANGE, *PFILE_LEVEL_TRIM_RANGE
req.redist: 
---

# _FILE_LEVEL_TRIM_RANGE structure


## -description


Specifies a range of a file that is to be trimmed.


## -struct-fields




### -field Offset

Offset, in bytes, from the start of the file for the range to be trimmed.


### -field Length

Length, in bytes, for the range to be trimmed.


## -remarks



Before the trim operation is passed to the underlying storage system the input ranges are reduced to be 
    aligned to page boundaries (4,096 bytes on 32-bit and x64-based editions of Windows, 8,192 bytes on Itanium-Based 
    editions of Windows).




## -see-also




<a href="https://msdn.microsoft.com/2d466a98-f7b2-4638-942c-1cf9016d0bf9">FILE_LEVEL_TRIM</a>



<a href="https://msdn.microsoft.com/3d293d09-8d41-495d-9095-f2f24bf6ac6b">FILE_LEVEL_TRIM_OUTPUT</a>



<b>FSCTL_FILE_LEVEL_TRIM</b>
 

 

