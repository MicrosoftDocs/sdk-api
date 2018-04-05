---
UID: NS:winioctl._FILE_LEVEL_TRIM_OUTPUT
title: "_FILE_LEVEL_TRIM_OUTPUT"
author: windows-driver-content
description: Used as output to the FSCTL_FILE_LEVEL_TRIM control code.
old-location: fs\file_level_trim_output.htm
old-project: FileIO
ms.assetid: 3d293d09-8d41-495d-9095-f2f24bf6ac6b
ms.author: windowsdriverdev
ms.date: 3/29/2018
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
req.typenames: FILE_LEVEL_TRIM_OUTPUT, *PFILE_LEVEL_TRIM_OUTPUT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	FILE_LEVEL_TRIM_OUTPUT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _FILE_LEVEL_TRIM_OUTPUT structure


## -description


Used as output to the 
    <a href="https://msdn.microsoft.com/library/windows/hardware/hh451098">FSCTL_FILE_LEVEL_TRIM</a> control code.


## -struct-fields




### -field NumRangesProcessed

Contains the number of ranges that were successfully processed. This may be less than the value passed in 
      the <b>NumRanges</b> member of the 
      <a href="https://msdn.microsoft.com/library/windows/hardware/hh406398">FILE_LEVEL_TRIM</a> structure. If it is then the last 
      ranges in the array were not processed.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh451098">FSCTL_FILE_LEVEL_TRIM</a>
 

 

