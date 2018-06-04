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
 

 

