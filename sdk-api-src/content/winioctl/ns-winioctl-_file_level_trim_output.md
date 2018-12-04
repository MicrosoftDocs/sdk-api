---
UID: NS:winioctl._FILE_LEVEL_TRIM_OUTPUT
title: "_FILE_LEVEL_TRIM_OUTPUT"
author: windows-sdk-content
description: Used as output to the FSCTL_FILE_LEVEL_TRIM control code.
old-location: fs\file_level_trim_output.htm
tech.root: fileio
ms.assetid: 3d293d09-8d41-495d-9095-f2f24bf6ac6b
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: "*PFILE_LEVEL_TRIM_OUTPUT, FILE_LEVEL_TRIM_OUTPUT, FILE_LEVEL_TRIM_OUTPUT structure [Files], PFILE_LEVEL_TRIM_OUTPUT, PFILE_LEVEL_TRIM_OUTPUT structure pointer [Files], _FILE_LEVEL_TRIM_OUTPUT, fs.file_level_trim_output, winioctl/FILE_LEVEL_TRIM_OUTPUT, winioctl/PFILE_LEVEL_TRIM_OUTPUT"
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
 - FILE_LEVEL_TRIM_OUTPUT
product: Windows
targetos: Windows
req.typenames: FILE_LEVEL_TRIM_OUTPUT, *PFILE_LEVEL_TRIM_OUTPUT
req.redist: 
---

# _FILE_LEVEL_TRIM_OUTPUT structure


## -description


Used as output to the 
    <a href="https://msdn.microsoft.com/2d466a98-f7b2-4638-942c-1cf9016d0bf9">FSCTL_FILE_LEVEL_TRIM</a> control code.


## -struct-fields




### -field NumRangesProcessed

Contains the number of ranges that were successfully processed. This may be less than the value passed in 
      the <b>NumRanges</b> member of the 
      <a href="https://msdn.microsoft.com/2d466a98-f7b2-4638-942c-1cf9016d0bf9">FILE_LEVEL_TRIM</a> structure. If it is then the last 
      ranges in the array were not processed.


## -see-also




<a href="https://msdn.microsoft.com/2d466a98-f7b2-4638-942c-1cf9016d0bf9">FSCTL_FILE_LEVEL_TRIM</a>
 

 

