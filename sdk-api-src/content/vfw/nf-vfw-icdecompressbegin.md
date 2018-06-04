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

# ICDecompressBegin macro


## -description



The <b>ICDecompressBegin</b> macro notifies a video decompression driver to prepare to decompress data. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/24cd5220-d473-4968-8678-b00670eecf8f">ICM_DECOMPRESS_BEGIN</a> message.




## -parameters




### -param hic

Handle to a decompressor. 


### -param lpbiInput

Pointer to a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure containing the input format. 


### -param lpbiOutput

Pointer to a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure containing the output format. 


## -remarks



When the driver receives this message, it should allocate buffers and do any time-consuming operations so that it can process <a href="https://msdn.microsoft.com/666f2ebf-80a5-4846-861d-c79c3001c5a0">ICM_DECOMPRESS</a> messages efficiently.

The <b>ICDecompressBegin</b> and <a href="https://msdn.microsoft.com/9d66174a-b6bd-4bcd-a88a-bb1876bbc510">ICDecompressEnd</a> macros do not nest. If your driver receives <a href="https://msdn.microsoft.com/24cd5220-d473-4968-8678-b00670eecf8f">ICM_DECOMPRESS_BEGIN</a> before decompression is stopped with <a href="https://msdn.microsoft.com/16ce2424-9606-455f-afbd-84326457538e">ICM_DECOMPRESS_END</a>, it should restart decompression with new parameters.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

