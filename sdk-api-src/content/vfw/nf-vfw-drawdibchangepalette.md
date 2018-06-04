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

# DrawDibChangePalette function


## -description



The <b>DrawDibChangePalette</b> function sets the palette entries used for drawing DIBs.




## -parameters




### -param hdd

Handle to a DrawDib DC.


### -param iStart

Starting palette entry number.


### -param iLen

Number of palette entries.


### -param lppe

Pointer to an array of palette entries.


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise.




## -remarks



This function changes the physical palette only if the current DrawDib palette is realized by calling the <a href="https://msdn.microsoft.com/4723c8a4-36af-4543-b6df-d51f68a3e94d">DrawDibRealize</a> function.

If the color table is not changed, the next call to the <a href="https://msdn.microsoft.com/b503fcd8-e928-4b3c-9ff5-96b88c5fb2f4">DrawDibDraw</a> function that does not specify DDF_SAME_DRAW calls the <a href="https://msdn.microsoft.com/89178e33-e440-49fe-9900-0baea229d289">DrawDibBegin</a> function implicitly.




## -see-also




<a href="https://msdn.microsoft.com/9ba47b8d-5328-477e-9272-21e897e54348">DrawDib Functions</a>
 

 

