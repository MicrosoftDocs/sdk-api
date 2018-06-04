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

# ICameraControl::get_PanTilt


## -description


The <code>get_PanTilt</code> method returns the camera's pan and tilt angles.


## -parameters




### -param pPanValue [out]

Receives the current panning angle, in arc seconds. An arc second is 1/3600th of a degree. See <a href="https://msdn.microsoft.com/4cbf7582-63ad-4572-be62-be1fe5bc60b3">ICameraControl::get_Pan</a>.


### -param pTiltValue [out]

Receives the current tilt angle, in arc seconds. See <a href="https://msdn.microsoft.com/8e9d9176-fb27-4221-876b-49f407289877">ICameraControl::get_Tilt</a>.


### -param pFlags [out]

Receives one or more flags. See <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a>.


## -returns



Returns an <b>HRESULT</b> value.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/7046f96d-a613-4056-84dd-be022efdda4f">ICameraControl Interface</a>
 

 

