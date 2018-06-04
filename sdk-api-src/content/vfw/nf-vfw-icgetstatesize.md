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

# ICGetStateSize macro


## -description



The <b>ICGetStateSize</b> macro queries a video compression driver to determine the amount of memory required to retrieve the configuration information. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/4b77e294-f3aa-45f9-a4f4-f103b83eae8d">ICM_GETSTATE</a> message.




## -parameters




### -param hic

Handle of the compressor. 


## -remarks



The structure used to represent configuration information is driver specific and is defined by the driver.

Use <b>ICGetStateSize</b> before calling the <a href="https://msdn.microsoft.com/e0066cc2-a67d-4cf4-9d22-506cc152ec14">ICGetState</a> macro to determine the size of buffer to allocate for the call.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

