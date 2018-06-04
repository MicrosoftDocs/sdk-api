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

# WICJpegScanType enumeration


## -description


Specifies the memory layout of pixel data in a JPEG image scan. 


## -enum-fields




### -field WICJpegScanTypeInterleaved

The pixel data is stored in an interleaved memory layout.


### -field WICJpegScanTypePlanarComponents

The pixel data is stored in a planar memory layout.


### -field WICJpegScanTypeProgressive

The pixel data is stored in a progressive layout.


### -field WICJpegScanType_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 


## -see-also




<a href="https://msdn.microsoft.com/DC8B42F0-66D3-4425-9AA8-6B8F0D9B8568">WICJpegScanType</a>
 

 

