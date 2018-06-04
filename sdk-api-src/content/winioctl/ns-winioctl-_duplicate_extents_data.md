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
 

 

