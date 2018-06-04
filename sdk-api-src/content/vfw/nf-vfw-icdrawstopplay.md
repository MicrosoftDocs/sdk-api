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

# ICDrawStopPlay macro


## -description



The <b>ICDrawStopPlay</b> macro notifies a rendering driver when a play operation is complete. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/cfe2ee98-80d0-4554-bcbd-9873769da674">ICM_DRAW_STOP_PLAY</a> message.




## -parameters




### -param hic

Handle to a driver. 


## -remarks



Use this message when the play operation is complete. Use the <a href="https://msdn.microsoft.com/c8608410-da45-4953-b16a-050870f85af9">ICDrawStop</a> macro to end timing.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

