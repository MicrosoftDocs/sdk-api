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

# SmoothingMode enumeration


## -description


The <b>SmoothingMode</b> enumeration specifies the type of smoothing (antialiasing) that is applied to lines and curves. This enumeration is used by the <a href="https://msdn.microsoft.com/85aacaa3-3a08-4879-8f49-7d082269cbe4">Graphics::GetSmoothingMode</a> and <a href="https://msdn.microsoft.com/d42ae7c7-9381-4613-bb65-76683873a63a">Graphics::SetSmoothingMode</a> methods of the 
			<a href="https://msdn.microsoft.com/library/windows/hardware/mt131452">Graphics</a> class.


## -enum-fields




### -field SmoothingModeInvalid

Reserved.


### -field SmoothingModeDefault

Specifies that smoothing is not applied.


### -field SmoothingModeHighSpeed

Specifies that smoothing is not applied.


### -field SmoothingModeHighQuality

Specifies that smoothing is applied using an 8 X 4 box filter.


### -field SmoothingModeNone

Specifies that smoothing is not applied.


### -field SmoothingModeAntiAlias

Specifies that smoothing is applied using an 8 X 4 box filter.


### -field SmoothingModeAntiAlias8x4

Specifies that smoothing is applied using an 8 X 4 box filter.


### -field SmoothingModeAntiAlias8x8

Specifies that smoothing is applied using an 8 X 8 box filter.


## -remarks



Smoothing performed by an 8 X 4 box filter gives better results for nearly vertical lines than it does for nearly horizontal lines. Smoothing performed by an 8 X 8 box filter gives equally good results for nearly vertical and nearly horizontal lines. The 8x8 algorithm produces higher quality smoothing but is slower than the 8 X 4 algorithm.




## -see-also




<a href="https://msdn.microsoft.com/85aacaa3-3a08-4879-8f49-7d082269cbe4">Graphics::GetSmoothingMode</a>



<a href="https://msdn.microsoft.com/d42ae7c7-9381-4613-bb65-76683873a63a">Graphics::SetSmoothingMode</a>
 

 

