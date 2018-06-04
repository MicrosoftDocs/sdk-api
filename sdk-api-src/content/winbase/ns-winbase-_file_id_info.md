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
 

 

