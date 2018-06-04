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

# SaveDC function


## -description


The <b>SaveDC</b> function saves the current state of the specified device context (DC) by copying data describing selected objects and graphic modes (such as the bitmap, brush, palette, font, pen, region, drawing mode, and mapping mode) to a context stack.


## -parameters




### -param hdc [in]

A handle to the DC whose state is to be saved.


## -returns



If the function succeeds, the return value identifies the saved state.

If the function fails, the return value is zero.




## -remarks



The <b>SaveDC</b> function can be used any number of times to save any number of instances of the DC state.

A saved state can be restored by using the <a href="https://msdn.microsoft.com/7043edbb-b3ea-4946-a2ba-cae356b04d1d">RestoreDC</a> function.




## -see-also




<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/7043edbb-b3ea-4946-a2ba-cae356b04d1d">
        RestoreDC
      </a>
 

 

