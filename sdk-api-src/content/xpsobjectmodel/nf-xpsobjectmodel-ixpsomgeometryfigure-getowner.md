---
UID: NF:xpsobjectmodel.IXpsOMGeometryFigure.GetOwner
title: IXpsOMGeometryFigure::GetOwner method
author: windows-driver-content
description: Gets a pointer to the IXpsOMGeometry interface that contains the geometry figure.
old-location: xps\ixpsomgeometryfigure_getowner.htm
old-project: printdocs
ms.assetid: 520e52ff-fb65-430f-972c-40ca2ab959b2
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetOwner method [XPS Documents and Packaging], GetOwner method [XPS Documents and Packaging], IXpsOMGeometryFigure interface, GetOwner,IXpsOMGeometryFigure.GetOwner, IXpsOMGeometryFigure, IXpsOMGeometryFigure interface [XPS Documents and Packaging], GetOwner method, IXpsOMGeometryFigure::GetOwner, xps.ixpsomgeometryfigure_getowner, xpsobjectmodel/IXpsOMGeometryFigure::GetOwner
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
-	IXpsOMGeometryFigure.GetOwner
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGeometryFigure::GetOwner method


## -description


Gets a pointer to the <a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a> interface that contains the geometry figure.


## -parameters




### -param owner [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a> interface that contains the geometry figure. If the interface is not assigned to a geometry, a <b>NULL</b> pointer is returned.


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
<i>owner</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d3f74c1e-49ef-40ee-a2f4-b6d198b57624">IXpsOMGeometry</a>



<a href="https://msdn.microsoft.com/e76a14ce-cfc3-4a50-855e-f5779b9fc261">IXpsOMGeometryFigure</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>
 

 

