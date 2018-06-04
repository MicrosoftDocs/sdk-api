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

# ICDrawQuery macro


## -description



The <b>ICDrawQuery</b> macro queries a rendering driver to determine if it can render data in a specific format. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/b829a04b-c1be-47c6-96e9-a6dc6f802811">ICM_DRAW_QUERY</a> message.




## -parameters




### -param hic

Handle to a driver. 


### -param lpbiInput

Pointer to a <a href="https://msdn.microsoft.com/84cc51e8-78f3-4ee6-bc08-94feff89afb0">BITMAPINFO</a> structure containing the input format. 


## -remarks



This macro differs from the <a href="https://msdn.microsoft.com/52a43888-9839-45a3-b139-e84943c345c2">ICDrawBegin</a> macro in that it queries the driver in a general sense. <b>ICDrawBegin</b> determines if the driver can draw the data using the specified format under specific conditions, such as stretching the image.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

