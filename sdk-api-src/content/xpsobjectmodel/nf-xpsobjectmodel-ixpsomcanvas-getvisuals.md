---
UID: NF:xpsobjectmodel.IXpsOMCanvas.GetVisuals
title: IXpsOMCanvas::GetVisuals
author: windows-sdk-content
description: Gets a pointer to an IXpsOMVisualCollection interface that contains a collection of the visual objects in the canvas.
old-location: xps\ixpsomcanvas_getvisuals.htm
tech.root: printdocs
ms.assetid: 67f42c32-f9d2-4d64-a8e1-b18a0d5f55fa
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetVisuals, GetVisuals method [XPS Documents and Packaging], GetVisuals method [XPS Documents and Packaging],IXpsOMCanvas interface, IXpsOMCanvas interface [XPS Documents and Packaging],GetVisuals method, IXpsOMCanvas.GetVisuals, IXpsOMCanvas::GetVisuals, xps.ixpsomcanvas_getvisuals, xpsobjectmodel/IXpsOMCanvas::GetVisuals
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMCanvas.GetVisuals
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMCanvas::GetVisuals


## -description


Gets a pointer to an <a href="https://msdn.microsoft.com/f373b437-3973-40aa-9cac-a6b196a3e5d1">IXpsOMVisualCollection</a> interface that contains a collection of the visual objects in the canvas.


## -parameters




### -param visuals [out, retval]

The collection of the visual objects in the canvas. If no visual objects are attached to the canvas, an empty collection is returned.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>visuals</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3cb0e1b3-88a8-4724-a3c5-0df416294e62">IXpsOMCanvas</a>



<a href="https://msdn.microsoft.com/f373b437-3973-40aa-9cac-a6b196a3e5d1">IXpsOMVisualCollection</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

