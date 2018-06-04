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

# MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAGS enumeration


## -description


Specifies the content protection requirements for a video frame.


## -enum-fields




### -field MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_PROTECTED

The video frame should be protected.


### -field MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_REQUIRES_SURFACE_PROTECTION

Direct3D surface protection must be applied to any surface that contains the frame.


### -field MF_MEDIA_ENGINE_FRAME_PROTECTION_FLAG_REQUIRES_ANTI_SCREEN_SCRAPE_PROTECTION

Direct3D anti-screen-scrape protection must be applied to any surface that contains the frame.


## -see-also




<a href="https://msdn.microsoft.com/4D67813D-F222-4EB1-B059-6DB5EC642DA2">IMFMediaEngineProtectedContent::GetRequiredProtections</a>



<a href="https://msdn.microsoft.com/3A5C6908-65F4-4E7A-AD71-BBD1C2A4ACE3">IMFMediaEngineProtectedContent::TransferVideoFrame</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

