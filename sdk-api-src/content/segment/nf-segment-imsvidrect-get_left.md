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

# IMSVidRect::get_Left


## -description


The <b>get_Left</b> method retrieves the left x-coordinate of the rectangle. This coordinate is relative to the rectangle's associated window.


## -parameters




### -param LeftVal






#### - pLeftVal [out]

Pointer to a variable that receives the left x-coordinate, in pixels.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/0b3cf31b-e0cc-4208-a128-b77460fc0f1b">IMSVidRect Interface</a>



<a href="https://msdn.microsoft.com/caa56beb-7eba-48a1-8645-f63666ba0593">IMSVidRect::get_HWnd</a>



<a href="https://msdn.microsoft.com/8e61fd8a-9ea0-48c1-8749-780b0363c12d">IMSVidRect::put_Left</a>
 

 

