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

# IMixerPinConfig::GetZOrder


## -description



The <code>GetZOrder</code> method retrieves the z-order of a particular video stream.



This method is not currently implemented and returns E_NOTIMPL.


## -parameters




### -param pdwZOrder [out]

Pointer to a value indicating the order in which streams will clip each other.


## -returns



Returns E_NOTIMPL.




## -remarks



Images with larger z-values are always in front of images with smaller z-values.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/6a4f3462-4596-4f02-a41f-47161f8aa4db">IMixerPinConfig Interface</a>



<a href="https://msdn.microsoft.com/fe8e71b8-9aaf-438e-b370-5ba9f131bf7a">IMixerPinConfig::SetZOrder</a>
 

 

