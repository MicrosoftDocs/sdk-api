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

# PenType enumeration


## -description


The <b>PenType</b> enumeration indicates the type of pattern, texture, or gradient that a pen draws. 


## -enum-fields




### -field PenTypeSolidColor

Indicates that the pen draws with a solid color. 


### -field PenTypeHatchFill

Indicates that the pen draws with a hatch pattern that is specified by a 
				<a href="https://msdn.microsoft.com/6e633cb2-8b0f-4b6a-95d8-f494d5f972eb">HatchBrush</a> object. 


### -field PenTypeTextureFill

Indicates that the pen draws with a texture that is specified by a 
				<a href="https://msdn.microsoft.com/4657ed8b-9cec-49ba-bf20-545bf3ee51f9">TextureBrush</a> object. 


### -field PenTypePathGradient

Indicates that the pen draws with a color gradient that is specified by a 
				<a href="https://msdn.microsoft.com/cac0a3ce-982e-4de5-a160-cb8a755beddd">PathGradientBrush</a> object. 


### -field PenTypeLinearGradient

Indicates that the pen draws with a color gradient that is specified by a 
				<a href="https://msdn.microsoft.com/43901cd3-b059-4830-9063-e8287899e18a">LinearGradientBrush</a> object. 


### -field PenTypeUnknown

Indicates that the pen type is unknown. 


## -remarks



A pen's type is determined when the pen is constructed. For example, if you pass a 
				<a href="https://msdn.microsoft.com/6e633cb2-8b0f-4b6a-95d8-f494d5f972eb">HatchBrush</a> object to a 
				<a href="https://msdn.microsoft.com/b48affa5-d953-478c-b651-0534db4d2b78">Pen</a> constructor, then the pen that is constructed has a pen type of <b><b>PenTypeHatchFill</b></b>. If you pass a 
				<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a> object or a 
				<a href="https://msdn.microsoft.com/8d5c8780-f03c-40b2-b237-e40121e3d6f6">SolidBrush</a> object to a 
				<b>Pen</b> constructor, then the pen that is constructed has a pen type of <b><b>PenTypeSolidColor</b></b>. 



