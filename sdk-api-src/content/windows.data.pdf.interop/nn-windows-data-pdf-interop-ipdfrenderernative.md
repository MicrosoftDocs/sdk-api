---
UID: NN:windows.data.pdf.interop.IPdfRendererNative
title: IPdfRendererNative (windows.data.pdf.interop.h)

description: Represents a high-performance API for displaying a single page of a Portable Document Format (PDF) file.
old-location: winrt\ipdfrenderernative.htm
tech.root: WinRT
ms.assetid: 96a00afb-e957-4e49-8f30-d6a3d639680f

ms.date: 12/05/2018
ms.keywords: IPdfRendererNative, IPdfRendererNative interface [Windows Runtime], IPdfRendererNative interface [Windows Runtime],described, windows/IPdfRendererNative, winrt.ipdfrenderernative
ms.topic: interface
f1_keywords: 
 - "windows.data.pdf.interop/IPdfRendererNative"
dev_langs:
 - c++
req.header: windows.data.pdf.interop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Windows.data.pdf.interop.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windows.data.pdf.lib
req.dll: Windows.Data.Pdf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windows.Data.Pdf.dll
api_name:
 - IPdfRendererNative
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPdfRendererNative interface


## -description


Represents a high-performance API for  displaying a single page of a  Portable Document Format (PDF) file.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPdfRendererNative</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPdfRendererNative</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPdfRendererNative</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.data.pdf.interop/nf-windows-data-pdf-interop-ipdfrenderernative-renderpagetodevicecontext">RenderPageToDeviceContext</a>
</td>
<td align="left" width="63%">
Outputs a single page of a PDF file as a bitmap image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/windows.data.pdf.interop/nf-windows-data-pdf-interop-ipdfrenderernative-renderpagetosurface">RenderPageToSurface</a>
</td>
<td align="left" width="63%">
Outputs a single page of a PDF file to a DirectX image-data object.

</td>
</tr>
</table> 


## -remarks



This API is specifically designed for DirectX apps that use C++ and Extensible Application Markup Language (XAML).

To get an instance of the <b>IPdfRendererNative</b> interface, call the <a href="https://docs.microsoft.com/windows/desktop/api/windows.data.pdf.interop/nf-windows-data-pdf-interop-pdfcreaterenderer">PdfCreateRenderer</a> function.



