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

# ICDecompressEnd macro


## -description



The <b>ICDecompressEnd</b> macro notifies a video decompression driver to end decompression and free resources allocated for decompression. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/16ce2424-9606-455f-afbd-84326457538e">ICM_DECOMPRESS_END</a> message.




## -parameters




### -param hic

Handle to a decompressor. 


## -remarks



The driver should free any resources allocated for the <a href="https://msdn.microsoft.com/24cd5220-d473-4968-8678-b00670eecf8f">ICM_DECOMPRESS_BEGIN</a> message.

The <a href="https://msdn.microsoft.com/3e9fb4b7-bdc6-402c-a5c6-3f837149c291">ICDecompressBegin</a> and <b>ICDecompressEnd</b> macros do not nest. If your driver receives <a href="https://msdn.microsoft.com/24cd5220-d473-4968-8678-b00670eecf8f">ICM_DECOMPRESS_BEGIN</a> before decompression is stopped with <a href="https://msdn.microsoft.com/16ce2424-9606-455f-afbd-84326457538e">ICM_DECOMPRESS_END</a>, it should restart decompression with new parameters.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

