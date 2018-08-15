---
UID: NF:xpsobjectmodel.IXpsOMGeometryFigure.GetIsFilled
title: IXpsOMGeometryFigure::GetIsFilled
author: windows-sdk-content
description: Gets a value that indicates whether the figure is filled.
old-location: xps\ixpsomgeometryfigure_getisfilled.htm
old-project: printdocs
ms.assetid: 22da5239-c79f-4306-ad60-9b3e5bcae988
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: FALSE, GetIsFilled, GetIsFilled method [XPS Documents and Packaging], GetIsFilled method [XPS Documents and Packaging],IXpsOMGeometryFigure interface, IXpsOMGeometryFigure interface [XPS Documents and Packaging],GetIsFilled method, IXpsOMGeometryFigure.GetIsFilled, IXpsOMGeometryFigure::GetIsFilled, TRUE, xps.ixpsomgeometryfigure_getisfilled, xpsobjectmodel/IXpsOMGeometryFigure::GetIsFilled
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.redist: 
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
 - IXpsOMGeometryFigure.GetIsFilled
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGeometryFigure::GetIsFilled


## -description


Gets a value that indicates whether the figure is filled.


## -parameters




### -param isFilled [out, retval]

The Boolean value that indicates whether the figure is filled.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
The figure is filled by a brush.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
The figure is not filled.

</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK; otherwise, it returns an <b>HRESULT</b> error code.

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
<i>isFilled</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This value corresponds to that of the <b>IsFilled</b> attribute of the <b>PathFigure</b> element in the document markup.




## -see-also




<a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

