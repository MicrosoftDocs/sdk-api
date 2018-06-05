---
UID: NS:winioctl._FILE_ZERO_DATA_INFORMATION
title: "_FILE_ZERO_DATA_INFORMATION"
author: windows-sdk-content
description: Contains a range of a file to set to zeros.
old-location: fs\file_zero_data_information_str.htm
old-project: FileIO
ms.assetid: ad2c4e2d-7f41-45e8-beff-2f6d735f152e
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: "*PFILE_ZERO_DATA_INFORMATION, FILE_ZERO_DATA_INFORMATION, FILE_ZERO_DATA_INFORMATION structure [Files], PFILE_ZERO_DATA_INFORMATION, PFILE_ZERO_DATA_INFORMATION structure pointer [Files], _FILE_ZERO_DATA_INFORMATION, _win32_file_zero_data_information_str, base.file_zero_data_information_str, fs.file_zero_data_information_str, winioctl/FILE_ZERO_DATA_INFORMATION, winioctl/PFILE_ZERO_DATA_INFORMATION"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FILE_ZERO_DATA_INFORMATION, *PFILE_ZERO_DATA_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	FILE_ZERO_DATA_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _FILE_ZERO_DATA_INFORMATION structure


## -description


Contains a range of a file to set to zeros. This structure is used by the 
<a href="https://msdn.microsoft.com/library/windows/hardware/mt668765">FSCTL_SET_ZERO_DATA</a> control code


## -struct-fields




### -field FileOffset

The file offset of the start of the range to set to zeros, in bytes.


### -field BeyondFinalZero

The byte offset of the first byte beyond the last zeroed byte.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt668765">FSCTL_SET_ZERO_DATA</a>



<a href="https://msdn.microsoft.com/7326041d-f11e-4b80-ac4e-07173e418ce7">Sparse Files</a>
 

 

