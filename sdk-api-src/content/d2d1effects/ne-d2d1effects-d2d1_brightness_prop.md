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

# D2D1_BRIGHTNESS_PROP enumeration


## -description


Identifiers for the properties of the <a href="https://msdn.microsoft.com/5088D4D4-DFC8-45D3-B1C3-D576742D931C">Brightness effect</a>.


## -enum-fields




### -field D2D1_BRIGHTNESS_PROP_WHITE_POINT

The upper portion of the brightness transfer curve. The white point adjusts the appearance of the brighter portions of the image. 
          This property is for both the x value and the y value, in that order. Each of the values of this property are between 0 and 1, inclusive.
          

The type is <a href="https://msdn.microsoft.com/DD180090-D2F4-4DF3-8652-101713C01AE4">D2D1_VECTOR_2F</a>.

The default value is (1.0f, 1.0f).


### -field D2D1_BRIGHTNESS_PROP_BLACK_POINT

The lower portion of the brightness transfer curve. The black point adjusts the appearance of the darker portions of the image. 
          This property is for both the x value and the y value, in that order. Each of the values of this property are between 0 and 1, inclusive.
          

The type is <a href="https://msdn.microsoft.com/DD180090-D2F4-4DF3-8652-101713C01AE4">D2D1_VECTOR_2F</a>.

The default value is (0.0f, 0.0f).


### -field D2D1_BRIGHTNESS_PROP_FORCE_DWORD



