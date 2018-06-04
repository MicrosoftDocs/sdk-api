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

# _DXVAHD_ITELECINE_CAPS enumeration


## -description


Specifies the inverse telecine (IVTC) capabilities of a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.


## -enum-fields




### -field DXVAHD_ITELECINE_CAPS_32

The video processor can reverse 3:2 pulldown.


### -field DXVAHD_ITELECINE_CAPS_22

The video processor can reverse 2:2 pulldown.


### -field DXVAHD_ITELECINE_CAPS_2224

The video processor can reverse 2:2:2:4 pulldown.


### -field DXVAHD_ITELECINE_CAPS_2332

The video processor can reverse 2:3:3:2 pulldown.


### -field DXVAHD_ITELECINE_CAPS_32322

The video processor can reverse 3:2:3:2:2 pulldown.


### -field DXVAHD_ITELECINE_CAPS_55

The video processor can reverse 5:5 pulldown.


### -field DXVAHD_ITELECINE_CAPS_64

The video processor can reverse 6:4 pulldown.


### -field DXVAHD_ITELECINE_CAPS_87

The video processor can reverse 8:7 pulldown.


### -field DXVAHD_ITELECINE_CAPS_222222222223

The video processor can reverse 2:2:2:2:2:2:2:2:2:2:2:3 pulldown.


### -field DXVAHD_ITELECINE_CAPS_OTHER

The video processor can reverse other telecine modes not listed here.


## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/41959498-501d-4f0d-ba1f-1c0690b62f4d">Direct3D Video Enumerations</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

