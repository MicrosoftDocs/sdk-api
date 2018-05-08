---
UID: NF:xpsobjectmodel.IXpsOMGeometry.GetFigures
title: IXpsOMGeometry::GetFigures
author: windows-driver-content
description: Gets a pointer to the geometry's IXpsOMGeometryFigureCollection interface, which contains the collection of figures that make up this geometry.
old-location: xps\ixpsomgeometry_getfigures.htm
old-project: printdocs
ms.assetid: c49566d6-8a37-4ad6-9b3a-52ef39b925be
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetFigures, GetFigures method [XPS Documents and Packaging], GetFigures method [XPS Documents and Packaging],IXpsOMGeometry interface, IXpsOMGeometry interface [XPS Documents and Packaging],GetFigures method, IXpsOMGeometry.GetFigures, IXpsOMGeometry::GetFigures, xps.ixpsomgeometry_getfigures, xpsobjectmodel/IXpsOMGeometry::GetFigures
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: XPS_INTERLEAVING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMGeometry.GetFigures
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGeometry::GetFigures


## -description


Gets a pointer to the geometry's <a href="https://msdn.microsoft.com/24ed79ff-9160-4e9b-b322-c538b30f113b">IXpsOMGeometryFigureCollection</a> interface, which  contains the collection of  figures that make up this geometry.


## -parameters




### -param figures [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/24ed79ff-9160-4e9b-b322-c538b30f113b">IXpsOMGeometryFigureCollection</a> interface.


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
<i>figures</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a>



<a href="https://msdn.microsoft.com/24ed79ff-9160-4e9b-b322-c538b30f113b">IXpsOMGeometryFigureCollection</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

