---
UID: NF:windows.data.pdf.interop.PdfRenderParams
title: PdfRenderParams function (windows.data.pdf.interop.h)
description: Populates a PDF_RENDER_PARAMS structure. A PDF_RENDER_PARAMS structure represents a set of properties for outputting a single page of a Portable Document Format (PDF) file.
helpviewer_keywords: ["PdfRenderParams","PdfRenderParams function [Windows Runtime]","windows/PdfRenderParams","winrt.pdfrenderparams"]
old-location: winrt\pdfrenderparams.htm
tech.root: WinRT
ms.assetid: 5C229DEF-DAF7-414B-B733-4807E4122C16
ms.date: 12/05/2018
ms.keywords: PdfRenderParams, PdfRenderParams function [Windows Runtime], windows/PdfRenderParams, winrt.pdfrenderparams
req.header: windows.data.pdf.interop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windows.data.pdf.lib
req.dll: Windows.Data.Pdf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PdfRenderParams
 - windows.data.pdf.interop/PdfRenderParams
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Windows.Data.Pdf.dll
api_name:
 - PdfRenderParams
---

# PdfRenderParams function


## -description

Populates a <a href="/windows/desktop/api/windows.data.pdf.interop/ns-windows-data-pdf-interop-pdf_render_params">PDF_RENDER_PARAMS</a> structure. A PDF_RENDER_PARAMS structure represents a set of properties for outputting a single page of a Portable Document Format (PDF) file.

## -parameters

### -param srcRect [in]

The rectangular portion of the original page, as defined by the D2D_RECT_F structure's upper-left and lower-right corner x- and y-coordinates. The default value is 0.f for all coordinates.

### -param destinationWidth [in]

The specified width of the page. The default is 0.f.

### -param destinationHeight [in]

The specified height of the page. The default is 0.f.

### -param bkColor [in]

The specified background color of the page. The default is {1.f, 1.f, 1.f, 1.f}, which represents the values 1.0 for red, green, blue, and alpha channel, respectively. These values, taken together, represent white at full opacity.

### -param ignoreHighContrast [in]

False to use the system's high contrast display settings; otherwise true. The default is true.

## -returns

Represents a set of properties for outputting a single page of a Portable Document Format (PDF) file.