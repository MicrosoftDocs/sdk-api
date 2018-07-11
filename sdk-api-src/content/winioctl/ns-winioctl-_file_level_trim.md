---
UID: NS:winioctl._FILE_LEVEL_TRIM
title: "_FILE_LEVEL_TRIM"
author: windows-sdk-content
description: Used as input to the FSCTL_FILE_LEVEL_TRIM control code.
old-location: fs\file_level_trim.htm
old-project: fileio
ms.assetid: db3ac916-83e7-4aa1-b5aa-dab139a0a21a
ms.author: windowssdkdev
ms.date: 06/14/2018
ms.keywords: "*PFILE_LEVEL_TRIM, FILE_LEVEL_TRIM, FILE_LEVEL_TRIM structure [Files], PFILE_LEVEL_TRIM, PFILE_LEVEL_TRIM structure pointer [Files], _FILE_LEVEL_TRIM, fs.file_level_trim, winioctl/FILE_LEVEL_TRIM, winioctl/PFILE_LEVEL_TRIM"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FILE_LEVEL_TRIM, *PFILE_LEVEL_TRIM
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _FILE_LEVEL_TRIM structure


## -description


Used as input to the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/hh451098">FSCTL_FILE_LEVEL_TRIM</a> control code.


## -struct-fields




### -field Key

Reserved. Set to zero (0).


### -field NumRanges

Number of <a href="https://msdn.microsoft.com/library/windows/hardware/hh406405">FILE_LEVEL_TRIM_RANGE</a> entries in 
      the <b>Ranges</b> member. On return should be compared with the 
      <b>NumRangesProcessed</b> member of the 
      <a href="https://msdn.microsoft.com/library/windows/hardware/hh406402">FILE_LEVEL_TRIM_OUTPUT</a> structure.


### -field Ranges

Array of ranges that describe the portions of the file that are to be trimmed.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh406402">FILE_LEVEL_TRIM_OUTPUT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh406405">FILE_LEVEL_TRIM_RANGE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh451098">FSCTL_FILE_LEVEL_TRIM</a>
 

 

