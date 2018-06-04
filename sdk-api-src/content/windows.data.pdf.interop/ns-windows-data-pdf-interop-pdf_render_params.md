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

# PDF_RENDER_PARAMS structure


## -description


Represents a set of properties for outputting a single page of a Portable Document Format (PDF) file.


## -struct-fields




### -field pdf.interop.PDF_RENDER_PARAMS.SourceRect

 


### -field pdf.interop.PDF_RENDER_PARAMS.DestinationWidth

 


### -field pdf.interop.PDF_RENDER_PARAMS.DestinationHeight

 


### -field pdf.interop.PDF_RENDER_PARAMS.BackgroundColor

 


### -field pdf.interop.PDF_RENDER_PARAMS.IgnoreHighContrast

 




#### - BackgroundColor

Outputs the page with the specified background color. The default is {1.f, 1.f, 1.f, 1.f}, which represents the values 1.0 for red, green, blue, and alpha channel, respectively. These values, taken together, represent white at full opacity.


#### - DestinationHeight

Outputs the page at the specified height. The default is 0.f.


#### - DestinationWidth

Outputs the page at the specified width. The default is 0.f.


#### - IgnoreHighContrast

False to use the system's high contrast display settings; otherwise true. The default is true.


#### - SourceRect

Outputs a rectangular portion of the original page, as defined by the <b>D2D_RECT_F</b> structure's upper-left and lower-right corner x- and y-coordinates. The default value is 0.f for all coordinates.


## -remarks



This structure is used by the <a href="https://msdn.microsoft.com/5ec97d21-3160-48e7-9486-a8ea9ca9df92">RenderPageToDeviceContext</a> and <a href="https://msdn.microsoft.com/d4688c23-0122-40a7-908e-793c3f03fb37">RenderPageToSurface</a> methods.



