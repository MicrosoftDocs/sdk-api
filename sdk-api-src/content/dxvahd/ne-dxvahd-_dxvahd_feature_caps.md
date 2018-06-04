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

# _DXVAHD_FEATURE_CAPS enumeration


## -description


Defines features that a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device can support.


## -enum-fields




### -field DXVAHD_FEATURE_CAPS_ALPHA_FILL

The device can set the alpha values on the video output. See <a href="https://msdn.microsoft.com/dcd42210-d5f8-42c7-aac0-08f0ce4b7ac9">DXVAHD_BLT_STATE_ALPHA_FILL_DATA</a>.


### -field DXVAHD_FEATURE_CAPS_CONSTRICTION

The device can downsample the video output. See <a href="https://msdn.microsoft.com/962a99bd-060d-4101-b65a-d0406e136bf7">DXVAHD_BLT_STATE_CONSTRICTION_DATA</a>.


### -field DXVAHD_FEATURE_CAPS_LUMA_KEY

The device can perform luma keying. See <a href="https://msdn.microsoft.com/d94b04d9-9d94-4392-a0bf-a33210aeef1f">DXVAHD_STREAM_STATE_LUMA_KEY_DATA</a>.


### -field DXVAHD_FEATURE_CAPS_ALPHA_PALETTE

The device can apply alpha values from color palette entries. See <a href="https://msdn.microsoft.com/51135d6e-4f97-44d9-b1d5-f7d2095ee6f1">DXVAHD_STREAM_STATE_ALPHA_DATA</a>.


## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/41959498-501d-4f0d-ba1f-1c0690b62f4d">Direct3D Video Enumerations</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

