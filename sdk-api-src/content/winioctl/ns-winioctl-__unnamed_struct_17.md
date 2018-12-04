---
UID: NS:winioctl.__unnamed_struct_17
title: READ_FILE_USN_DATA
author: windows-sdk-content
description: Specifies the versions of the update sequence number (USN) change journal supported by the application.
old-location: fs\read_file_usn_data.htm
tech.root: fileio
ms.assetid: 8c403eec-7504-4a69-9f05-7a3a164557a6
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: "*PREAD_FILE_USN_DATA, PREAD_FILE_USN_DATA, PREAD_FILE_USN_DATA structure pointer [Files], READ_FILE_USN_DATA, READ_FILE_USN_DATA structure [Files], fs.read_file_usn_data, winioctl/PREAD_FILE_USN_DATA, winioctl/READ_FILE_USN_DATA"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
 - READ_FILE_USN_DATA
product: Windows
targetos: Windows
req.typenames: READ_FILE_USN_DATA, *PREAD_FILE_USN_DATA
req.redist: 
---

# READ_FILE_USN_DATA structure


## -description


Specifies the versions of the update sequence number (USN) change journal supported by the 
    application. This structure is the input structure to the 
    <a href="https://msdn.microsoft.com/22c797c8-87c8-4d45-b163-4573e6ed17e1">FSCTL_READ_FILE_USN_DATA</a> control code.


## -struct-fields




### -field MinMajorVersion

The lowest version of the USN change journal accepted by the application. If the input buffer is not 
      specified this defaults to 2.


### -field MaxMajorVersion

The highest version of the USN change journal accepted by the application. If the input buffer is not 
      specified this defaults to 2. To support 128-bit file identifiers used by ReFS this must be 3 or higher.


## -see-also




<a href="https://msdn.microsoft.com/205de464-7e96-477b-9115-e819719b160e">FSCTL_READ_USN_JOURNAL</a>



<a href="https://msdn.microsoft.com/bbde9dfb-c205-4432-be71-250d73b881f1">Volume Management Structures</a>
 

 

