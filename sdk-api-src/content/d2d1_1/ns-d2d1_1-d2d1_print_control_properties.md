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

# D2D1_PRINT_CONTROL_PROPERTIES structure


## -description


The creation properties for a <a href="https://msdn.microsoft.com/0E8D8218-0671-44A2-AD6E-13BB0B4EB66C">ID2D1PrintControl</a> object.


## -struct-fields




### -field fontSubset

Type: <b><a href="https://msdn.microsoft.com/B8361117-6018-48EE-AD3D-2A37F6B71293">D2D1_PRINT_FONT_SUBSET_MODE</a></b>

The mode to use for subsetting fonts for printing, defaults to <a href="https://msdn.microsoft.com/B8361117-6018-48EE-AD3D-2A37F6B71293">D2D1_PRINT_FONT_SUBSET_MODE_DEFAULT</a>.


### -field rasterDPI

Type: <b>FLOAT</b>

DPI for rasterization of all unsupported Direct2D commands or options, defaults to 150.0.


### -field colorSpace

Type: <b><a href="https://msdn.microsoft.com/2c90978b-8a5a-4e5d-9ced-e0ec917271ff">D2D1_COLOR_SPACE</a></b>

Color space for vector graphics, defaults to <a href="https://msdn.microsoft.com/2c90978b-8a5a-4e5d-9ced-e0ec917271ff">D2D1_COLOR_SPACE_SRGB</a>.

