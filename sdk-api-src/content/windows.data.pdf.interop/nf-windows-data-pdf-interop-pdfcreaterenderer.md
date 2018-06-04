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



