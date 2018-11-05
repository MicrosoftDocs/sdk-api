---
UID: NF:windows.data.pdf.interop.PdfCreateRenderer
title: PdfCreateRenderer function
author: windows-sdk-content
description: Gets an instance of the IPdfRendererNative interface for displaying a single page of a Portable Document Format (PDF) file.
old-location: winrt\pdfcreaterenderer.htm
tech.root: WinRT
ms.assetid: 6C61B35A-FD43-434F-BD56-C912E2FCE464
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: PdfCreateRenderer, PdfCreateRenderer function [Windows Runtime], windows/PdfCreateRenderer, winrt.pdfcreaterenderer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: windows.data.pdf.interop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Windows.Data.Pdf.dll
api_name:
 - PdfCreateRenderer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PdfCreateRenderer function


## -description


Gets an instance of the <a href="https://msdn.microsoft.com/96a00afb-e957-4e49-8f30-d6a3d639680f">IPdfRendererNative</a> interface for displaying a single page of a Portable Document Format (PDF) file.


## -parameters




### -param pDevice [in]

An instance of a  Microsoft DirectX Graphics Infrastructure (DXGI) object that is used for producing image data.


### -param ppRenderer [out]

An instance of the high-performance <a href="https://msdn.microsoft.com/96a00afb-e957-4e49-8f30-d6a3d639680f">IPdfRendererNative</a> interface for  rendering PDF content on a DirectX surface.


## -returns



This function can return one of these values.

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
The function call succeeded.

</td>
</tr>
</table>
 




## -remarks



 This function is specifically designed for DirectX apps that use C++ and Extensible Application Markup Language (XAML).

The <b>PdfCreateRenderer</b> function should be called to display single pages of a PDF file,  one at a time. While you could call this function in parallel to display multiple pages at the same time, this could lead to unexpected results.



