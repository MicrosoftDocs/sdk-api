---
UID: NF:windows.data.pdf.interop.IPdfRendererNative.RenderPageToDeviceContext
title: IPdfRendererNative::RenderPageToDeviceContext (windows.data.pdf.interop.h)
description: The IPdfRendererNative::RenderPageToDeviceContext method outputs a single page of a Portable Document Format (PDF) file as a bitmap image.
helpviewer_keywords: ["IPdfRendererNative interface [Windows Runtime]","RenderPageToDeviceContext method","IPdfRendererNative.RenderPageToDeviceContext","IPdfRendererNative.pdf","IPdfRendererNative::RenderPageToDeviceContext","IPdfRendererNative::pdf","RenderPageToDeviceContext","RenderPageToDeviceContext method [Windows Runtime]","RenderPageToDeviceContext method [Windows Runtime]","IPdfRendererNative interface","windows/IPdfRendererNative::RenderPageToDeviceContext","winrt.ipdfrenderernative_renderpagetodevicecontext"]
old-location: winrt\ipdfrenderernative_renderpagetodevicecontext.htm
tech.root: WinRT
ms.assetid: 5ec97d21-3160-48e7-9486-a8ea9ca9df92
ms.date: 08/03/2022
ms.keywords: IPdfRendererNative interface [Windows Runtime],RenderPageToDeviceContext method, IPdfRendererNative.RenderPageToDeviceContext, IPdfRendererNative.pdf, IPdfRendererNative::RenderPageToDeviceContext, IPdfRendererNative::pdf, RenderPageToDeviceContext, RenderPageToDeviceContext method [Windows Runtime], RenderPageToDeviceContext method [Windows Runtime],IPdfRendererNative interface, windows/IPdfRendererNative::RenderPageToDeviceContext, winrt.ipdfrenderernative_renderpagetodevicecontext
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
req.lib: Windows.data.pdf.lib
req.dll: Windows.Data.Pdf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPdfRendererNative::RenderPageToDeviceContext
 - windows.data.pdf.interop/IPdfRendererNative::RenderPageToDeviceContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windows.Data.Pdf.dll
api_name:
 - IPdfRendererNative.RenderPageToDeviceContext
---

# IPdfRendererNative::RenderPageToDeviceContext (windows.data.pdf.interop.h)


## -description

Outputs a single page of a Portable Document Format (PDF) file as a bitmap image.

## -parameters

### -param pdfPage [in]

The <b>IPdfPage</b> interface as an instance of the <a href="uwp/api/windows.data.pdf.pdfpage">PdfPage</a> class type-casted to the <b>IUnknown</b> interface, `page.as<IUnknown>().get()`, representing the page to be output.

### -param pD2DDeviceContext [in]

A set of state and command buffers for outputting the page as a bitmap image.

### -param pRenderParams [in, optional]

A set of page output properties, such as rendering only a portion of the page, rendering a scaled version of the page, setting the page's background color, and whether the page is shown in high contrast mode. 

Provide a null pointer for this parameter to specify default page output properties. For the list of defaults, see <a href="/windows/desktop/api/windows.data.pdf.interop/ns-windows-data-pdf-interop-pdf_render_params">PDF_RENDER_PARAMS</a>.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The page output operation succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/windows.data.pdf.interop/nn-windows-data-pdf-interop-ipdfrenderernative">IPdfRendererNative</a>
