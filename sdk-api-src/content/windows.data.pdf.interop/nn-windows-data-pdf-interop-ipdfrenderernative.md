---
UID: NN:windows.data.pdf.interop.IPdfRendererNative
title: IPdfRendererNative
author: windows-sdk-content
description: Represents a high-performance API for displaying a single page of a Portable Document Format (PDF) file.
old-location: winrt\ipdfrenderernative.htm
tech.root: WinRT
ms.assetid: 96a00afb-e957-4e49-8f30-d6a3d639680f
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IPdfRendererNative, IPdfRendererNative interface [Windows Runtime], IPdfRendererNative interface [Windows Runtime],described, windows/IPdfRendererNative, winrt.ipdfrenderernative
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPdfRendererNative interface


## -description


Represents a high-performance API for  displaying a single page of a  Portable Document Format (PDF) file.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPdfRendererNative</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPdfRendererNative</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5ec97d21-3160-48e7-9486-a8ea9ca9df92">RenderPageToDeviceContext</a>
</td>
<td align="left" width="63%">
Outputs a single page of a PDF file as a bitmap image.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4688c23-0122-40a7-908e-793c3f03fb37">RenderPageToSurface</a>
</td>
<td align="left" width="63%">
Outputs a single page of a PDF file to a DirectX image-data object.

</td>
</tr>
</table> 


## -remarks



This API is specifically designed for DirectX apps that use C++ and Extensible Application Markup Language (XAML).

To get an instance of the <b>IPdfRendererNative</b> interface, call the <a href="https://msdn.microsoft.com/6C61B35A-FD43-434F-BD56-C912E2FCE464">PdfCreateRenderer</a> function.



