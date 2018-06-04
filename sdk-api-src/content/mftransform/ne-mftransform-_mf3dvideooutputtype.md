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

# _MF3DVideoOutputType enumeration


## -description


Specifies how to  output a 3D stereoscopic video stream.


## -enum-fields




### -field MF3DVideoOutputType_BaseView

Output the base view only. Discard the other view.


### -field MF3DVideoOutputType_Stereo

Output a stereo view (two buffers).


## -remarks



This enumeration is used with the <a href="https://msdn.microsoft.com/AA75A2FB-DEAC-44E9-93E9-4AC2D9F03B39">MF_ENABLE_3DVIDEO_OUTPUT</a> attribute.




## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

