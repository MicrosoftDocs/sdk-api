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

# ICGetState macro


## -description



The <b>ICGetState</b> macro queries a video compression driver to return its current configuration in a block of memory. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/4b77e294-f3aa-45f9-a4f4-f103b83eae8d">ICM_GETSTATE</a> message.




## -parameters




### -param hic

Handle of the compressor. 


### -param pv

Pointer to a block of memory to contain the current configuration information. You can specify <b>NULL</b> for this parameter to determine the amount of memory required for the configuration information, as in <a href="https://msdn.microsoft.com/386761e8-9234-4541-b593-ce8e323714bf">ICGetStateSize</a>. 


### -param cb

Size, in bytes, of the block of memory. 


## -remarks



The <a href="https://msdn.microsoft.com/386761e8-9234-4541-b593-ce8e323714bf">ICGetStateSize</a> macro returns the number of bytes used by the state data.

The structure used to represent configuration information is driver specific and is defined by the driver.

Use <a href="https://msdn.microsoft.com/386761e8-9234-4541-b593-ce8e323714bf">ICGetStateSize</a> before calling the <b>ICGetState</b> macro to determine the size of buffer to allocate for the call.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

