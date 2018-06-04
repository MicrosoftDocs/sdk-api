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

# _MFVideoDRMFlags enumeration


## -description


Specifies the type of copy protection required for a video stream.
        


## -enum-fields




### -field MFVideoDRMFlag_None

No copy protection is required.
          


### -field MFVideoDRMFlag_AnalogProtected

Analog copy protection should be applied.
          


### -field MFVideoDRMFlag_DigitallyProtected

Digital copy protection should be applied.
          


## -remarks



Use these flags with the <a href="https://msdn.microsoft.com/fb12ba38-a4f4-44fe-bf31-e731c56bb145">MF_MT_DRM_FLAGS</a> attribute.




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

