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

# GetColorAdjustment function


## -description


The <b>GetColorAdjustment</b> function retrieves the color adjustment values for the specified device context (DC).


## -parameters




### -param hdc [in]

A handle to the device context.


### -param lpca [out]

A pointer to a <a href="https://msdn.microsoft.com/9a080f60-0bce-46b6-b8a8-f534ff83a0a8">COLORADJUSTMENT</a> structure that receives the color adjustment values.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/9a080f60-0bce-46b6-b8a8-f534ff83a0a8">COLORADJUSTMENT</a>



<a href="https://msdn.microsoft.com/9dd32d4a-30bd-406f-a934-bb71ad4ca2cb">Color Functions</a>



<a href="https://msdn.microsoft.com/d1a25f13-6b47-4be7-927b-814dd6ae81f8">Colors Overview</a>



<a href="https://msdn.microsoft.com/292d6cdc-cafa-438a-9392-a9c22e7d44a5">SetColorAdjustment</a>
 

 

