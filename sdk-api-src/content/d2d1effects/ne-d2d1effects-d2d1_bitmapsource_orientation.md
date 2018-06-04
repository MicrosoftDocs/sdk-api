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

# D2D1_BITMAPSOURCE_ORIENTATION enumeration


## -description



          Speficies whether a flip and/or rotation operation should be performed by the <a href="https://msdn.microsoft.com/86646111-208A-4E6D-A28C-7B23A1742D24">Bitmap source effect</a>



## -enum-fields




### -field D2D1_BITMAPSOURCE_ORIENTATION_DEFAULT

The effect doesn't change the orientation of the input.


### -field D2D1_BITMAPSOURCE_ORIENTATION_FLIP_HORIZONTAL

Flips the image horizontally.


### -field D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE180

Rotates the image clockwise 180 degrees.


### -field D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE180_FLIP_HORIZONTAL

Rotates the image clockwise 180 degrees and flips it horizontally.


### -field D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE270_FLIP_HORIZONTAL

Rotates the image clockwise 270 degrees and flips it horizontally.


### -field D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE90

Rotates the image clockwise 90 degrees.


### -field D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE90_FLIP_HORIZONTAL

Rotates the image clockwise 90 degrees and flips it horizontally. 


### -field D2D1_BITMAPSOURCE_ORIENTATION_ROTATE_CLOCKWISE270

Rotates the image clockwise 270 degrees.


### -field D2D1_BITMAPSOURCE_ORIENTATION_FORCE_DWORD



