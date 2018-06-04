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

# tagCURSORSHAPE structure


## -description


Contains information about a cursor.


## -struct-fields




### -field xHotSpot

Type: <b>int</b>

The horizontal position of the hot spot, relative to the upper-left corner of the cursor bitmap. 


### -field yHotSpot

Type: <b>int</b>

The vertical position of the hot spot, relative to the upper-left corner of the cursor bitmap. 


### -field cx

Type: <b>int</b>

The width, in pixels, of the cursor. 


### -field cy

Type: <b>int</b>

The height, in pixels, of the cursor. 


### -field cbWidth

Type: <b>int</b>

The width, in bytes, of the cursor bitmap. 


### -field Planes

Type: <b>BYTE</b>

The number of color planes. 


### -field BitsPixel

Type: <b>BYTE</b>

The number of bits used to indicate the color of a single pixel in the cursor. 


## -remarks



When an application passes a cursor handle to the <a href="https://msdn.microsoft.com/a2385605-ad73-4250-ad78-36255144b816">LockResource</a>
				 function, the function returns a pointer to a buffer containing information about the cursor. An application can use the <b>CURSORSHAPE</b> structure to access the information.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/a2385605-ad73-4250-ad78-36255144b816">LockResource</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/ff321356-c999-4021-a537-fbe863996e24">Resources</a>
 

 

