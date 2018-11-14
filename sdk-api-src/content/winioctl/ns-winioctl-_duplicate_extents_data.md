---
UID: NS:winioctl._DUPLICATE_EXTENTS_DATA
title: "_DUPLICATE_EXTENTS_DATA"
author: windows-sdk-content
description: Contains parameters for the FSCTL_DUPLICATE_EXTENTS control code that performs the Block Cloning operation.
old-location: fs\duplicate_extents_data.htm
tech.root: fileio
ms.assetid: 9E2B3AA1-BC28-4458-9882-13F7EFB23756
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: "*PDUPLICATE_EXTENTS_DATA, DUPLICATE_EXTENTS_DATA, DUPLICATE_EXTENTS_DATA structure [Files], PDUPLICATE_EXTENTS_DATA, PDUPLICATE_EXTENTS_DATA structure pointer [Files], _DUPLICATE_EXTENTS_DATA, fs.duplicate_extents_data, winioctl/DUPLICATE_EXTENTS_DATA, winioctl/PDUPLICATE_EXTENTS_DATA"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - DUPLICATE_EXTENTS_DATA
product: Windows
targetos: Windows
req.typenames: DUPLICATE_EXTENTS_DATA, *PDUPLICATE_EXTENTS_DATA
req.redist: 
---

# _DUPLICATE_EXTENTS_DATA structure


## -description


Contains parameters for the <a href="https://msdn.microsoft.com/D66D2172-9308-4138-A321-867589787FED">FSCTL_DUPLICATE_EXTENTS</a> control code that performs the <a href="https://msdn.microsoft.com/E18E8D79-3985-40B8-A4C5-A73A21E5C527">Block Cloning</a> operation.


## -struct-fields




### -field FileHandle

A handle to the source file from which the byte range is to be copied.
To retrieve a file handle, use the <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function.



### -field SourceFileOffset

The offset, in bytes, to the beginning of the range to copy from the source file.


### -field TargetFileOffset

The offset, in bytes, to place the copied byte range in the destination file.


### -field ByteCount

The length, in bytes, of the range to copy.


## -see-also




<a href="https://msdn.microsoft.com/E18E8D79-3985-40B8-A4C5-A73A21E5C527">Block Cloning</a>



<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>



<a href="https://msdn.microsoft.com/D66D2172-9308-4138-A321-867589787FED">FSCTL_DUPLICATE_EXTENTS_TO_FILE</a>



<a href="https://msdn.microsoft.com/e27ded4b-d104-4244-b38e-5fed10d32e1e">File Management Control Codes</a>
 

 

