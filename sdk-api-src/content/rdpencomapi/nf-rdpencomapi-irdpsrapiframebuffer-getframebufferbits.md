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

# IRDPSRAPIFrameBuffer::GetFrameBufferBits


## -description


Gets the bits in a specified area of the frame.


## -parameters




### -param x [in]

The x coordinate of the requested area of the frame.


### -param y [in]

The y coordinate of the requested area of the frame.


### -param Width [in]

The width of the requested area of the frame.


### -param Heigth [in]

The height of the requested area of the frame.


### -param ppBits






#### - pbBits [out, retval]

The contents of the frame buffer in the specified area.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://msdn.microsoft.com/ab40bdd2-448f-4867-aabd-d6b66add5247">IRDPSRAPIFrameBuffer</a>
 

 

