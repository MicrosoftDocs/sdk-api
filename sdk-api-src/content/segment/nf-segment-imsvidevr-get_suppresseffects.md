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

# IMSVidEVR::get_SuppressEffects


## -description


The <b>get_SuppressEffects</b> method queries whether the <a href="https://msdn.microsoft.com/743a1950-4f70-45a1-9536-0d75064f401b">Video Control</a> configures the system for optimal video playback


## -parameters




### -param bSuppress [out]

Receives a <b>VARIANT_BOOL</b>. For more information, see <a href="https://msdn.microsoft.com/399250b6-4f2d-4dbf-b1e8-d32a0673617e">IMSVidEVR::put_SuppressEffects</a>. The default value is VARIANT_TRUE.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/437f515b-0353-4ff2-b8c2-5dd27d4e12f7">IMSVidEVR</a>
 

 

