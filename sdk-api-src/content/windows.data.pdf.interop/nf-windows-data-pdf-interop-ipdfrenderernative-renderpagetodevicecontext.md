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

# IPdfRendererNative::pdf


## -description


Outputs a single page of a Portable Document Format (PDF) file as a bitmap image.


## -parameters




### -param pdfPage [in]

The <b>IPdfPage</b> interface as an instance of the <a href="https://msdn.microsoft.com/85bf8d83-8c70-472f-8762-709fddaf3222">PdfPage</a> class,  type-casted to the <b>IUnknown</b> interface, representing the page to be output.


### -param pD2DDeviceContext [in]

A set of state and command buffers for outputting the page as a bitmap image.


### -param pRenderParams [in, optional]

A set of page output properties, such as rendering only a portion of the page, rendering a scaled version of the page, setting the page's background color, and whether the page is shown in high contrast mode. 

Provide a null pointer for this parameter to specify default page output properties. For the list of defaults, see <a href="https://msdn.microsoft.com/1B2F12FB-E053-4B79-B71D-E66D7A6E5054">PDF_RENDER_PARAMS</a>.


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




<a href="https://msdn.microsoft.com/96a00afb-e957-4e49-8f30-d6a3d639680f">IPdfRendererNative</a>
 

 

