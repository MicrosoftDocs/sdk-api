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

# ICDrawEnd macro


## -description



The <b>ICDrawEnd</b> macro notifies a rendering driver to decompress the current image to the screen and to release resources allocated for decompression and drawing. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/03910752-6122-4a5a-84ff-2cecf66cf439">ICM_DRAW_END</a> message.




## -parameters




### -param hic

Handle to a driver. 


## -remarks



The <a href="https://msdn.microsoft.com/e5ecd7dd-376b-422c-bbb8-4e7c41e3cac8">ICM_DRAW_BEGIN</a> and <a href="https://msdn.microsoft.com/03910752-6122-4a5a-84ff-2cecf66cf439">ICM_DRAW_END</a> messages do not nest. If your driver receives <b>ICM_DRAW_BEGIN</b> before decompression is stopped with <b>ICM_DRAW_END</b>, it should restart decompression with new parameters.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

