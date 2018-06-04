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

# D2D1_TEMPERATUREANDTINT_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/8df72105-26ea-2dea-a4de-ef06902b7e0b">Temperature and Tint effect</a>.


## -enum-fields




### -field D2D1_TEMPERATUREANDTINT_PROP_TEMPERATURE

The D2D1_TEMPERATUREANDTINT_PROP_TEMPERATURE property is a float value specifying how much to increase or decrease the temperature of the input image.  The allowed range is -1.0 to 1.0. The default value is 0.0.


### -field D2D1_TEMPERATUREANDTINT_PROP_TINT

The D2D1_TEMPERATUREANDTINT_PROP_TINT propery is a float value specifying how much to increase or decrease the tint of the input image.  The allowed range is -1.0 to 1.0.  The default value is 0.0.


### -field D2D1_TEMPERATUREANDTINT_PROP_FORCE_DWORD



