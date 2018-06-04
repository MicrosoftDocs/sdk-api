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

# ICCompressBegin macro


## -description


The ICCompressBegin macro notifies a video compression driver to prepare to compress data. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/dd1d3a66-c625-4f55-b65a-8545c1c16301">ICM_COMPRESS_BEGIN</a> message.


## -parameters




### -param hic

Handle to a compressor.


### -param lpbiInput

Pointer to a <a href="https://msdn.microsoft.com/02f8ed65-8fed-4dda-9b94-7343a0cfa8c1">BITMAPINFO</a> structure containing the input format.


### -param lpbiOutput

Pointer to a <a href="https://msdn.microsoft.com/02f8ed65-8fed-4dda-9b94-7343a0cfa8c1">BITMAPINFO</a> structure containing the output format.


## -remarks



The driver should allocate and initialize any tables or memory that it needs for compressing the data formats when it receives the <a href="https://msdn.microsoft.com/d95b943f-458d-4a5e-bab1-e3648d323395">ICM_COMPRESS</a> message.

VCM saves the settings of the most recent <b>ICCompressBegin</b> macro. The <b>ICCompressBegin</b> and <b>ICCompressEnd</b> messages do not nest. If your driver receives <b>ICM_COMPRESS_BEGIN</b> before compression is stopped with <b>ICM_COMPRESS_END</b>, it should restart compression with new parameters.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

