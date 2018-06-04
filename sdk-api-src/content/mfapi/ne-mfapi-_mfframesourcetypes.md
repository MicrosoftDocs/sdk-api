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

# _MFFrameSourceTypes enumeration


## -description


Describes the type of data provided by a frame source.


## -enum-fields




### -field MFFrameSourceTypes_Color

The frame source provides color data.


### -field MFFrameSourceTypes_Infrared

The frame source provides infrared data.


### -field MFFrameSourceTypes_Depth

The frame source provides depth data.


### -field MFFrameSourceTypes_Image

The frame source provides image data.

<b>Note</b>  This value was added in Windows 10, version 1803.


### -field MFFrameSourceTypes_Custom

The frame source provides custom data.


## -remarks



The values of this enumeration are used with the <a href="https://msdn.microsoft.com/4A2B427E-E654-48BA-8BF4-16F1B1F8D266">MF_DEVICESTREAM_ATTRIBUTE_FRAMESOURCE_TYPES</a> attribute.



