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

# tagOLEDCFLAGS enumeration


## -description


Specifies additional information to the container about the device context that the object has requested.


## -enum-fields




### -field OLEDC_NODRAW

Indicates that the object will not use the returned <b>HDC</b> for drawing but merely to get information about the display device. In this case, the container can simply pass the window's device context without further processing.


### -field OLEDC_PAINTBKGND

Requests that the container paint the background behind the object before returning the device context. Objects should use this flag when requesting a device context to paint a transparent area.


### -field OLEDC_OFFSCREEN

Indicates that the object prefers to draw into an offscreen device context that should then be copied to the screen. The container can honor this request or not. If this bit is cleared, the container must return an on-screen device context allowing the object to perform direct screen operations such as showing a selection through an XOR operation. An object can specify this value when the drawing operation generates a lot of screen flicker.


## -see-also




<a href="https://msdn.microsoft.com/232587a8-ed88-4339-9e28-6e34be263a51">IOleInPlaceSiteWindowless::GetDC</a>
 

 

