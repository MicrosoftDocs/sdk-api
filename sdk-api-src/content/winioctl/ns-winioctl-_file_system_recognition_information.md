---
UID: NS:winioctl._FILE_SYSTEM_RECOGNITION_INFORMATION
title: "_FILE_SYSTEM_RECOGNITION_INFORMATION"
author: windows-driver-content
description: Contains file system recognition information retrieved by the FSCTL_QUERY_FILE_SYSTEM_RECOGNITION control code.
old-location: fs\file_system_recognition_information.htm
old-project: FileIO
ms.assetid: 27d9fd2b-d4c6-4237-8c15-0fa97b63b991
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: "*PFILE_SYSTEM_RECOGNITION_INFORMATION, FILE_SYSTEM_RECOGNITION_INFORMATION, FILE_SYSTEM_RECOGNITION_INFORMATION structure [Files], PFILE_SYSTEM_RECOGNITION_INFORMATION, PFILE_SYSTEM_RECOGNITION_INFORMATION structure pointer [Files], _FILE_SYSTEM_RECOGNITION_INFORMATION, fs.file_system_recognition_information, winioctl/FILE_SYSTEM_RECOGNITION_INFORMATION, winioctl/PFILE_SYSTEM_RECOGNITION_INFORMATION"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winioctl.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: FILE_SYSTEM_RECOGNITION_INFORMATION, *PFILE_SYSTEM_RECOGNITION_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinIoCtl.h
api_name:
-	FILE_SYSTEM_RECOGNITION_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _FILE_SYSTEM_RECOGNITION_INFORMATION structure


## -description


Contains file system recognition information retrieved by the <a href="https://msdn.microsoft.com/0b2ff131-a659-4bd0-b329-41fb60edbe13">FSCTL_QUERY_FILE_SYSTEM_RECOGNITION</a> control code.


## -struct-fields




### -field FileSystem

The file system name stored on the disk. This is a null-terminated string of 8 ASCII characters that represents the nonlocalizable human-readable name of the 
    file system the volume is formatted with.


## -see-also




<a href="https://msdn.microsoft.com/d9c19e01-ff82-4bbc-9eb6-aac9dc5c34ac">FILE_SYSTEM_RECOGNITION_STRUCTURE</a>



<a href="https://msdn.microsoft.com/0b2ff131-a659-4bd0-b329-41fb60edbe13">FSCTL_QUERY_FILE_SYSTEM_RECOGNITION</a>
 

 

