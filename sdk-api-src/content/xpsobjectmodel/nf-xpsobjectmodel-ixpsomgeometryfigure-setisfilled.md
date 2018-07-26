---
UID: NF:xpsobjectmodel.IXpsOMGeometryFigure.SetIsFilled
title: IXpsOMGeometryFigure::SetIsFilled
author: windows-sdk-content
description: Sets a value that indicates whether the figure is filled.
old-location: xps\ixpsomgeometryfigure_setisfilled.htm
old-project: printdocs
ms.assetid: 18054987-35a9-4049-ba0f-1425e2e54ed3
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: FALSE, IXpsOMGeometryFigure interface [XPS Documents and Packaging],SetIsFilled method, IXpsOMGeometryFigure.SetIsFilled, IXpsOMGeometryFigure::SetIsFilled, SetIsFilled, SetIsFilled method [XPS Documents and Packaging], SetIsFilled method [XPS Documents and Packaging],IXpsOMGeometryFigure interface, TRUE, xps.ixpsomgeometryfigure_setisfilled, xpsobjectmodel/IXpsOMGeometryFigure::SetIsFilled
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: XPS_INTERLEAVING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMGeometryFigure.SetIsFilled
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGeometryFigure::SetIsFilled


## -description


Sets a value that indicates whether the figure is filled.


## -parameters




### -param isFilled [in]

The value to be set.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The figure is filled by a brush.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The figure is not filled.

</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



In the document markup, the value returned in <i>isFilled</i>  corresponds to that of the <b>IsFilled</b> attribute of the <b>PathFigure</b> element.




## -see-also




<a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

