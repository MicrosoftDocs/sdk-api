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

# D2D1_DPICOMPENSATION_PROP enumeration


## -description



          Identifiers for properties of the <a href="https://msdn.microsoft.com/EA8AD89B-A710-468F-A6F3-474DA29586F1">DPI compensation effect</a>.
        


## -enum-fields




### -field D2D1_DPICOMPENSATION_PROP_INTERPOLATION_MODE


            The interpolation mode the effect uses to scale the image.
            

The type is <a href="https://msdn.microsoft.com/D47BE47D-09E3-46A5-8D89-884102EDEA9A">D2D1_DPICOMPENSATION_INTERPOLATION_MODE</a>.

The default value is D2D1_DPICOMPENSATION_INTERPOLATION_MODE_LINEAR.


### -field D2D1_DPICOMPENSATION_PROP_BORDER_MODE


            The mode used to calculate the border of the image, soft or hard. See Border modes for more info.
            

The type is <a href="https://msdn.microsoft.com/093C7028-9C0E-4BB5-9769-C456B7A23B6F">D2D1_BORDER_MODE</a>.

The default value is D2D1_BORDER_MODE_SOFT.


### -field D2D1_DPICOMPENSATION_PROP_INPUT_DPI


            The DPI of the input image.
            

The type is FLOAT.

The default value is 96.0f.


### -field D2D1_DPICOMPENSATION_PROP_FORCE_DWORD



