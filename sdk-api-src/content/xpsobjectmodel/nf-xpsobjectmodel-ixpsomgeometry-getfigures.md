---
UID: NF:xpsobjectmodel.IXpsOMGeometry.GetFigures
title: IXpsOMGeometry::GetFigures (xpsobjectmodel.h)
author: windows-sdk-content
description: Gets a pointer to the geometry's IXpsOMGeometryFigureCollection interface, which contains the collection of figures that make up this geometry.
old-location: xps\ixpsomgeometry_getfigures.htm
tech.root: printdocs
ms.assetid: c49566d6-8a37-4ad6-9b3a-52ef39b925be
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetFigures, GetFigures method [XPS Documents and Packaging], GetFigures method [XPS Documents and Packaging],IXpsOMGeometry interface, IXpsOMGeometry interface [XPS Documents and Packaging],GetFigures method, IXpsOMGeometry.GetFigures, IXpsOMGeometry::GetFigures, xps.ixpsomgeometry_getfigures, xpsobjectmodel/IXpsOMGeometry::GetFigures
ms.topic: method
f1_keywords: 
 - "xpsobjectmodel/IXpsOMGeometry.GetFigures"
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
 - IXpsOMGeometry.GetFigures
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMGeometry::GetFigures


## -description


Gets a pointer to the geometry's <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection">IXpsOMGeometryFigureCollection</a> interface, which  contains the collection of  figures that make up this geometry.


## -parameters




### -param figures [out, retval]

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection">IXpsOMGeometryFigureCollection</a> interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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
<i>figures</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry">IXpsOMGeometry</a>



<a href="https://docs.microsoft.com/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection">IXpsOMGeometryFigureCollection</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
 

 

