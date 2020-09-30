---
UID: NS:windows.data.pdf.interop.PDF_RENDER_PARAMS
title: PDF_RENDER_PARAMS (windows.data.pdf.interop.h)
description: Represents a set of properties for outputting a single page of a Portable Document Format (PDF) file.
helpviewer_keywords: ["PDF_RENDER_PARAMS","PDF_RENDER_PARAMS structure [Windows Runtime]","windows/PDF_RENDER_PARAMS","winrt.pdf_render_params"]
old-location: winrt\pdf_render_params.htm
tech.root: WinRT
ms.assetid: 1B2F12FB-E053-4B79-B71D-E66D7A6E5054
ms.date: 12/05/2018
ms.keywords: PDF_RENDER_PARAMS, PDF_RENDER_PARAMS structure [Windows Runtime], windows/PDF_RENDER_PARAMS, winrt.pdf_render_params
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PDF_RENDER_PARAMS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDF_RENDER_PARAMS
 - windows.data.pdf.interop/PDF_RENDER_PARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - windows.data.pdf.interop.h
api_name:
 - PDF_RENDER_PARAMS
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

### -field BackgroundColor

Outputs the page with the specified background color. The default is {1.f, 1.f, 1.f, 1.f}, which represents the values 1.0 for red, green, blue, and alpha channel, respectively. These values, taken together, represent white at full opacity.

### -field DestinationHeight

Outputs the page at the specified height. The default is 0.f.

### -field DestinationWidth

Outputs the page at the specified width. The default is 0.f.

### -field IgnoreHighContrast

False to use the system's high contrast display settings; otherwise true. The default is true.

### -field SourceRect

Outputs a rectangular portion of the original page, as defined by the <b>D2D_RECT_F</b> structure's upper-left and lower-right corner x- and y-coordinates. The default value is 0.f for all coordinates.

## -remarks

This structure is used by the <a href="/windows/desktop/api/windows.data.pdf.interop/nf-windows-data-pdf-interop-ipdfrenderernative-renderpagetodevicecontext">RenderPageToDeviceContext</a> and <a href="/windows/desktop/api/windows.data.pdf.interop/nf-windows-data-pdf-interop-ipdfrenderernative-renderpagetosurface">RenderPageToSurface</a> methods.