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

# D2D1_STRAIGHTEN_PROP enumeration


## -description


Identifiers for properties of the <a href="https://msdn.microsoft.com/aa37cdf1-bbb6-db4e-45a7-67c7cc16b7b4">Straighten effect</a>.


## -enum-fields




### -field D2D1_STRAIGHTEN_PROP_ANGLE

The D2D1_STRAIGHTEN_PROP_ANGLE property is a float value that specifies how much the image should be rotated.  The allowed range is -45.0 to 45.0.  The default value is 0.0.


### -field D2D1_STRAIGHTEN_PROP_MAINTAIN_SIZE

The D2D1_STRAIGHTEN_PROP_MAINTAIN_SIZE property is a boolean value that specifies whether the image will be scaled such that the original size is maintained without any invalid regions.
          The default value is True.


### -field D2D1_STRAIGHTEN_PROP_SCALE_MODE

The D2D1_STRAIGHTEN_PROP_SCALE_MODE property is a <a href="https://msdn.microsoft.com/EF6831AD-3D79-4A48-ACA5-7B8D80E8BAF3">D2D1_STRAIGHTEN_SCALE_MODE</a> enumeration value indicating the scaling mode that should be used.


### -field D2D1_STRAIGHTEN_PROP_FORCE_DWORD



