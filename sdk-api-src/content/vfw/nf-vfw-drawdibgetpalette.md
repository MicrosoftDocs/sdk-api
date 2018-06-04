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

# DrawDibGetPalette function


## -description



The <b>DrawDibGetPalette</b> function retrieves the palette used by a DrawDib DC.




## -parameters




### -param hdd

Handle to a DrawDib DC.


## -returns



Returns a handle to the palette if successful or <b>NULL</b> otherwise.




## -remarks



This function assumes the DrawDib DC contains a valid palette entry, implying that a call to this function must follow calls to the <a href="https://msdn.microsoft.com/b503fcd8-e928-4b3c-9ff5-96b88c5fb2f4">DrawDibDraw</a> or <a href="https://msdn.microsoft.com/89178e33-e440-49fe-9900-0baea229d289">DrawDibBegin</a> functions.

You should rarely need to call this function because you can realize the correct palette in response to a window message by using the <a href="https://msdn.microsoft.com/4723c8a4-36af-4543-b6df-d51f68a3e94d">DrawDibRealize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/9ba47b8d-5328-477e-9272-21e897e54348">DrawDib Functions</a>
 

 

