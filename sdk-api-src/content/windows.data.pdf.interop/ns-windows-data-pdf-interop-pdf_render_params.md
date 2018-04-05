---
UID: NS:windows.data.pdf.interop.PDF_RENDER_PARAMS
title: PDF_RENDER_PARAMS
author: windows-driver-content
description: Represents a set of properties for outputting a single page of a Portable Document Format (PDF) file.
old-location: winrt\pdf_render_params.htm
old-project: WinRT
ms.assetid: 1B2F12FB-E053-4B79-B71D-E66D7A6E5054
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: PDF_RENDER_PARAMS, PDF_RENDER_PARAMS structure [Windows Runtime], windows/PDF_RENDER_PARAMS, winrt.pdf_render_params
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: windows.data.pdf.interop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [UWP apps only]
req.target-min-winversvr: Windows Server 2012 R2 [UWP apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.data.pdf.interop.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PDF_RENDER_PARAMS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	windows.data.pdf.interop.h
api_name:
-	PDF_RENDER_PARAMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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



