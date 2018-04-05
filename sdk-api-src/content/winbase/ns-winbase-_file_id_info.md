---
UID: NS:winbase._FILE_ID_INFO
title: "_FILE_ID_INFO"
author: windows-driver-content
description: Contains identification information for a file.
old-location: fs\file_id_info.htm
old-project: FileIO
ms.assetid: e2774e29-1a90-44d6-9001-f73a98be6624
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: "*PFILE_ID_INFO, FILE_ID_INFO, FILE_ID_INFO structure [Files], PFILE_ID_INFO, PFILE_ID_INFO structure pointer [Files], _FILE_ID_INFO, fs.file_id_info, winbase/FILE_ID_INFO, winbase/PFILE_ID_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winbase.h
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
req.typenames: FILE_ID_INFO, *PFILE_ID_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinBase.h
api_name:
-	FILE_ID_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _FILE_ID_INFO structure


## -description


Contains identification information for a file. This structure is returned from the 
    <a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a> function when 
    <b>FileIdInfo</b> is passed in the <i>FileInformationClass</i> 
    parameter.


## -struct-fields




### -field VolumeSerialNumber

The serial number of the volume that contains a file.


### -field FileId

The 128-bit file identifier for the file. The file identifier and the volume serial number uniquely identify 
     a file on a single computer. To determine whether two open handles represent the same file, combine the 
     identifier and the volume serial number for each file and compare them.


## -see-also




<a href="https://msdn.microsoft.com/254ea6a9-e1dd-4b97-91f7-2693065c4bb8">FILE_ID_128</a>



<a href="https://msdn.microsoft.com/8f02e824-ca41-48c1-a5e8-5b12d81886b5">FILE_INFO_BY_HANDLE_CLASS</a>



<a href="https://msdn.microsoft.com/406d5c0f-b49a-4075-ac3e-c5b55a0c3fe9">File Management Structures</a>



<a href="https://msdn.microsoft.com/e261ea45-d084-490e-94b4-129bd76f6a04">GetFileInformationByHandleEx</a>
 

 

