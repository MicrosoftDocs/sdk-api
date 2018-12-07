---
UID: NF:xpsobjectmodel.IXpsOMMatrixTransform.SetMatrix
title: IXpsOMMatrixTransform::SetMatrix
author: windows-sdk-content
description: Sets the XPS_MATRIX structure, which specifies the transform matrix.
old-location: xps\ixpsommatrixtransform_setmatrix.htm
tech.root: printdocs
ms.assetid: cbe6a992-1c94-40b0-a0b6-3b214b928805
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IXpsOMMatrixTransform interface [XPS Documents and Packaging],SetMatrix method, IXpsOMMatrixTransform.SetMatrix, IXpsOMMatrixTransform::SetMatrix, SetMatrix, SetMatrix method [XPS Documents and Packaging], SetMatrix method [XPS Documents and Packaging],IXpsOMMatrixTransform interface, xps.ixpsommatrixtransform_setmatrix, xpsobjectmodel/IXpsOMMatrixTransform::SetMatrix
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IXpsOMMatrixTransform.SetMatrix
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMMatrixTransform::SetMatrix


## -description


Sets the <a href="https://msdn.microsoft.com/0df75410-0e34-4962-8499-879d5153d9af">XPS_MATRIX</a> structure, which specifies the transform matrix.


## -parameters




### -param matrix [in]

The address of the <a href="https://msdn.microsoft.com/0df75410-0e34-4962-8499-879d5153d9af">XPS_MATRIX</a> structure.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The matrix referenced by <i>matrix</i> is not valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d21457bc-9445-4ca2-ab9f-1e3f55e2e635">IXpsOMMatrixTransform</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/0df75410-0e34-4962-8499-879d5153d9af">XPS_MATRIX</a>
 

 

