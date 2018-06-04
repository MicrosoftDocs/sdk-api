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

# ICCompressGetFormat macro


## -description



The <b>ICCompressGetFormat</b> macro requests the output format of the compressed data from a video compression driver. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/ac12d415-bad5-4838-b206-09c8097d3fd9">ICM_COMPRESS_GET_FORMAT</a> message.




## -parameters




### -param hic

Handle of the compressor. 


### -param lpbiInput

Pointer to a BITMAPINFO structure containing the input format.


### -param lpbiOutput

Pointer to a BITMAPINFO structure containing the output format. 


## -remarks



If <i>lpbiOutput</i> is nonzero, the driver should fill the <b>BITMAPINFO</b> structure with the default output format corresponding to the input format specified for <i>lpbiInput</i>. If the compressor can produce several formats, the default format should be the one that preserves the greatest amount of information.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

