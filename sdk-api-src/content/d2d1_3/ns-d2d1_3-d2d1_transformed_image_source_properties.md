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

# D2D1_TRANSFORMED_IMAGE_SOURCE_PROPERTIES structure


## -description


Properties of a transformed image source.


## -struct-fields




### -field orientation

Type: <b><a href="https://msdn.microsoft.com/CFDE26F2-2D10-4B7E-A7B0-A2A86923116E">D2D1_ORIENTATION</a></b>

The orientation at which the image source is drawn.


### -field scaleX

Type: <b>FLOAT</b>

The horizontal scale factor at which the image source is drawn.


### -field scaleY

Type: <b>FLOAT</b>

The vertical scale factor at which the image source is drawn.


### -field interpolationMode

Type: <b><a href="https://msdn.microsoft.com/7a32f551-afad-4eb2-953f-a9acc71d7776">D2D1_INTERPOLATION_MODE</a></b>

The interpolation mode used when the image source is drawn.  This is ignored if the image source is drawn using the DrawImage method, or using an image brush.


### -field options

Type: <b><a href="https://msdn.microsoft.com/25A55F80-ACE0-4955-8483-687C7A7E4E20">D2D1_TRANSFORMED_IMAGE_SOURCE_OPTIONS</a></b>

Image sourc option flags.

