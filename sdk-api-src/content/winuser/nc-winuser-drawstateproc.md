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

# DRAWSTATEPROC callback function


## -description


The <b>DrawStateProc</b> function is an application-defined callback function that renders a complex image for the <a href="https://msdn.microsoft.com/b92150be-8264-4ea8-a2ea-d70b7fba6361">DrawState</a> function. The <b>DRAWSTATEPROC</b> type defines a pointer to this callback function. <b>DrawStateProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param hdc [in]

A handle to the device context to draw in. The device context is a memory device context with a bitmap selected, the dimensions of which are at least as great as those specified by the <i>cx</i> and <i>cy</i> parameters.


### -param lData [in]

Specifies information about the image, which the application passed to <a href="https://msdn.microsoft.com/b92150be-8264-4ea8-a2ea-d70b7fba6361">DrawState</a>.


### -param wData [in]

Specifies information about the image, which the application passed to <a href="https://msdn.microsoft.com/b92150be-8264-4ea8-a2ea-d70b7fba6361">DrawState</a>.


### -param cx [in]

The image width, in device units, as specified by the call to <a href="https://msdn.microsoft.com/b92150be-8264-4ea8-a2ea-d70b7fba6361">DrawState</a>.


### -param cy [in]

The image height, in device units, as specified by the call to <a href="https://msdn.microsoft.com/b92150be-8264-4ea8-a2ea-d70b7fba6361">DrawState</a>.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/b92150be-8264-4ea8-a2ea-d70b7fba6361">DrawState</a>



<a href="https://msdn.microsoft.com/ec18323e-c13b-4328-83bf-9e4ed4a712b8">Painting and Drawing Functions</a>



<a href="https://msdn.microsoft.com/8e6034af-4dea-4579-b476-52f6dd3d5bc7">Painting and Drawing Overview</a>
 

 

