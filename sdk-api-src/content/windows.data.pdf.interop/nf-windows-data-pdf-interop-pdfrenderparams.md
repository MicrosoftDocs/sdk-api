---
UID: NF:windows.data.pdf.interop.PdfRenderParams
title: PdfRenderParams function
author: windows-sdk-content
description: Populates a PDF_RENDER_PARAMS stucture. A PDF_RENDER_PARAMS structure represents a set of properties for outputting a single page of a Portable Document Format (PDF) file.
old-location: winrt\pdfrenderparams.htm
old-project: WinRT
ms.assetid: 5C229DEF-DAF7-414B-B733-4807E4122C16
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PdfRenderParams, PdfRenderParams function [Windows Runtime], windows/PdfRenderParams, winrt.pdfrenderparams
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: IP6_ADDRESS, *PIP6_ADDRESS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Windows.Data.Pdf.dll
api_name:
 - PdfRenderParams
product: Windows
targetos: Windows
req.lib: Windows.data.pdf.lib
req.dll: Windows.Data.Pdf.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# PdfRenderParams function


## -description


Populates a <a href="https://msdn.microsoft.com/1B2F12FB-E053-4B79-B71D-E66D7A6E5054">PDF_RENDER_PARAMS</a> stucture. A PDF_RENDER_PARAMS structure represents a set of properties for outputting a single page of a Portable Document Format (PDF) file.


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




