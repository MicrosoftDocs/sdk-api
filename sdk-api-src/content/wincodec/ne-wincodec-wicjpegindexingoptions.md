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

# WICJpegIndexingOptions enumeration


## -description


Specifies the options for indexing a JPEG image. 


## -enum-fields




### -field WICJpegIndexingOptionsGenerateOnDemand

Index generation is deferred until <a href="https://msdn.microsoft.com/d4908a75-e7de-4b8f-bdc8-d86cf6b49f8c">IWICBitmapSource::CopyPixels</a> is called on the image.


### -field WICJpegIndexingOptionsGenerateOnLoad

Index generation is performed when the when the image is initially loaded.


### -field WICJpegIndexingOptions_FORCE_DWORD

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. This value is not used. 


## -see-also




<a href="https://msdn.microsoft.com/D97A48E5-0398-460C-AFA9-2E1B8744926B">IWICJpegFrameDecode::SetIndexing</a>
 

 

