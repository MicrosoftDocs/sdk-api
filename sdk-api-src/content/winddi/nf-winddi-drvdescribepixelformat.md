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

# DrvDescribePixelFormat function


## -description


The <b>DrvDescribePixelFormat</b> function describes the pixel format for a device-specified <a href="https://msdn.microsoft.com/139a10e9-203b-499b-9291-8537eae9189c">PDEV</a> by writing a pixel format description to a PIXELFORMATDESCRIPTOR structure.


## -parameters




### -param dhpdev

Identifies the device for which pixel format information is requested.


### -param iPixelFormat

Specifies the index number of the requested pixel format.


### -param cjpfd

Specifies the maximum number of bytes that can be written to the structure pointed to by <i>ppfd</i>.


### -param ppfd

Pointer to a PIXELFORMATDESCRIPTOR structure (described in the Microsoft Windows SDK documentation) that is to receive information about the pixel format. This parameter can be <b>NULL</b>. 


## -returns



The return value is the maximum pixel format index if the function is successful. Otherwise, it is zero, and an error code is logged.




## -remarks



A display driver that supports 3D graphics hardware can support windows with different pixel formats on a single display surface. The pixel format must correspond to a configuration supported by the graphics hardware.

<b>DrvDescribePixelFormat</b> fills in the structure pointed to by <i>ppfd</i> if this parameter is not <b>NULL</b>.

The returned maximum pixel format index can be used by applications that need to obtain a device context's maximum pixel format index. The pixel formats that a device supports are identified by positive one-based integer indices.

The pixel format functions are used in conjunction with the window object services functions to track and update pixel formats of windows on a display surface.



