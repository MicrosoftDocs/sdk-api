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

# _MFVideoPadFlags enumeration


## -description



Specifies whether to pad a video image so that it fits within a specified aspect ratio.




## -enum-fields




### -field MFVideoPadFlag_PAD_TO_None

Do not pad the image.


### -field MFVideoPadFlag_PAD_TO_4x3

Pad the image so that it can be displayed in a 4×3 area.


### -field MFVideoPadFlag_PAD_TO_16x9

Pad the image so that it can be displayed in a 16×9 area.


## -remarks



Use these flags with the <a href="https://msdn.microsoft.com/d7fec5fb-a1fe-4cc9-aa27-a3af0456ea8d">MF_MT_PAD_CONTROL_FLAGS</a> attribute.




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

