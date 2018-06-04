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

# ColorRGBToHLS function


## -description


Converts colors from RGB to hue-luminance-saturation (HLS) format.


## -parameters




### -param clrRGB

Type: <b><a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a></b>

The original RGB color.


### -param pwHue [out]

Type: <b>WORD*</b>

A pointer to a value that, when this method returns successfully, receives the HLS hue value.


### -param pwLuminance [out]

Type: <b>WORD*</b>

A pointer to a value that, when this method returns successfully, receives the HLS luminance value.


### -param pwSaturation [out]

Type: <b>WORD*</b>

A pointer to a value that, when this method returns successfully, receives the HLS saturation value.


## -returns



This function does not return a value.



