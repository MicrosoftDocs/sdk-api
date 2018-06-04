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

# ColorAdjustLuma function


## -description


Changes the luminance of a RGB value. Hue and saturation are not affected.


## -parameters




### -param clrRGB

Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a></b>

The initial RGB value.


### -param n

Type: <b>int</b>

The luminance in units of 0.1 percent of the total range. For example, a value of <i>n</i> = 50 corresponds to 5 percent of the maximum luminance.


### -param fScale

Type: <b>BOOL</b>

If <i>fScale</i> is set to <b>TRUE</b>, <i>n</i> specifies how much to increment or decrement the current luminance. If <i>fScale</i> is set to <b>FALSE</b>, <i>n</i> specifies the absolute luminance.


## -returns



Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a></b>

Returns the modified RGB value.




## -remarks



If <i>fScale</i> is set to <b>TRUE</b>, <i>n</i> can range from -1000 to +1000.

If <i>fScale</i> is set to <b>FALSE</b>, <i>n</i> can range from 0 to 1000. Available luminance values range from 0 to a maximum. If the requested value is negative or exceeds the maximum, the luminance will be set to either zero or the maximum value, respectively.



