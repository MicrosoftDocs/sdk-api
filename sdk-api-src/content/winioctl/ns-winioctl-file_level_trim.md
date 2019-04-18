---
UID: NS:winioctl._FILE_LEVEL_TRIM
title: FILE_LEVEL_TRIM (winioctl.h)
author: windows-sdk-content
description: Used as input to the FSCTL_FILE_LEVEL_TRIM control code.
old-location: fs\file_level_trim.htm
tech.root: FileIO
ms.assetid: db3ac916-83e7-4aa1-b5aa-dab139a0a21a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PFILE_LEVEL_TRIM, FILE_LEVEL_TRIM, FILE_LEVEL_TRIM structure [Files], PFILE_LEVEL_TRIM, PFILE_LEVEL_TRIM structure pointer [Files], fs.file_level_trim, winioctl/FILE_LEVEL_TRIM, winioctl/PFILE_LEVEL_TRIM"
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
 - FILE_LEVEL_TRIM
product: Windows
targetos: Windows
req.typenames: FILE_LEVEL_TRIM, *PFILE_LEVEL_TRIM
req.redist: 
ms.custom: 19H1
---

# FILE_LEVEL_TRIM structure


## -description


Used as input to the 
    <a href="https://msdn.microsoft.com/2d466a98-f7b2-4638-942c-1cf9016d0bf9">FSCTL_FILE_LEVEL_TRIM</a> control code.


## -struct-fields




### -field Key

Reserved. Set to zero (0).


### -field NumRanges

Number of <a href="https://msdn.microsoft.com/2ee14239-68bb-40f6-b10b-2500d316dcc8">FILE_LEVEL_TRIM_RANGE</a> entries in 
      the <b>Ranges</b> member. On return should be compared with the 
      <b>NumRangesProcessed</b> member of the 
      <a href="https://msdn.microsoft.com/3d293d09-8d41-495d-9095-f2f24bf6ac6b">FILE_LEVEL_TRIM_OUTPUT</a> structure.


### -field Ranges

Array of ranges that describe the portions of the file that are to be trimmed.


## -see-also




<a href="https://msdn.microsoft.com/3d293d09-8d41-495d-9095-f2f24bf6ac6b">FILE_LEVEL_TRIM_OUTPUT</a>



<a href="https://msdn.microsoft.com/2ee14239-68bb-40f6-b10b-2500d316dcc8">FILE_LEVEL_TRIM_RANGE</a>



<a href="https://msdn.microsoft.com/2d466a98-f7b2-4638-942c-1cf9016d0bf9">FSCTL_FILE_LEVEL_TRIM</a>
 

 

