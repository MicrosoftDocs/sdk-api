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

# ICGetDefaultQuality macro


## -description



The <b>ICGetDefaultQuality</b> macro queries a video compression driver to provide its default quality setting. You can use this macro or explicitly call the <a href="https://msdn.microsoft.com/bba7f451-52c2-4684-a7c9-e4b05cb946c5">ICM_GETDEFAULTQUALITY</a> message.




## -parameters




### -param hic

Handle to a compressor. 


#### - wParam

Address to contain the default quality value. Quality values range from 0 to 10,000. 


## -remarks



The <b>ICGetDefaultQuality</b> macro returns the default quality value.




## -see-also




<a href="https://msdn.microsoft.com/e8ee41fa-180a-432a-933b-b4a525b9df8c">Video Compression Macros</a>



<a href="https://msdn.microsoft.com/df876309-68d3-43a3-9d83-6fdb8f345fdc">Video Compression Manager</a>
 

 

