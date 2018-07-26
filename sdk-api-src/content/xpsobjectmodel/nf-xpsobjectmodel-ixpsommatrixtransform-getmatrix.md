---
UID: NF:xpsobjectmodel.IXpsOMMatrixTransform.GetMatrix
title: IXpsOMMatrixTransform::GetMatrix
author: windows-sdk-content
description: Gets the XPS_MATRIX structure, which specifies the transform matrix.
old-location: xps\ixpsommatrixtransform_getmatrix.htm
old-project: printdocs
ms.assetid: 4067778d-d10f-4b53-9419-f438b7197f44
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: GetMatrix, GetMatrix method [XPS Documents and Packaging], GetMatrix method [XPS Documents and Packaging],IXpsOMMatrixTransform interface, IXpsOMMatrixTransform interface [XPS Documents and Packaging],GetMatrix method, IXpsOMMatrixTransform.GetMatrix, IXpsOMMatrixTransform::GetMatrix, xps.ixpsommatrixtransform_getmatrix, xpsobjectmodel/IXpsOMMatrixTransform::GetMatrix
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
 - IXpsOMMatrixTransform.GetMatrix
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMMatrixTransform::GetMatrix


## -description


Gets the <a href="https://msdn.microsoft.com/0df75410-0e34-4962-8499-879d5153d9af">XPS_MATRIX</a> structure, which specifies the transform matrix.


## -parameters




### -param matrix [out, retval]

The address of a variable that receives the <a href="https://msdn.microsoft.com/0df75410-0e34-4962-8499-879d5153d9af">XPS_MATRIX</a> structure.


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
<i>matrix</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/0df75410-0e34-4962-8499-879d5153d9af">XPS_MATRIX</a>
 

 

