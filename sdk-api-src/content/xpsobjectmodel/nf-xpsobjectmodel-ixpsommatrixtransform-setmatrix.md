---
UID: NF:xpsobjectmodel.IXpsOMMatrixTransform.SetMatrix
title: IXpsOMMatrixTransform::SetMatrix (xpsobjectmodel.h)
description: Sets the XPS_MATRIX structure, which specifies the transform matrix.
helpviewer_keywords: ["IXpsOMMatrixTransform interface [XPS Documents and Packaging]","SetMatrix method","IXpsOMMatrixTransform.SetMatrix","IXpsOMMatrixTransform::SetMatrix","SetMatrix","SetMatrix method [XPS Documents and Packaging]","SetMatrix method [XPS Documents and Packaging]","IXpsOMMatrixTransform interface","xps.ixpsommatrixtransform_setmatrix","xpsobjectmodel/IXpsOMMatrixTransform::SetMatrix"]
old-location: xps\ixpsommatrixtransform_setmatrix.htm
tech.root: xps
ms.assetid: cbe6a992-1c94-40b0-a0b6-3b214b928805
ms.date: 12/05/2018
ms.keywords: IXpsOMMatrixTransform interface [XPS Documents and Packaging],SetMatrix method, IXpsOMMatrixTransform.SetMatrix, IXpsOMMatrixTransform::SetMatrix, SetMatrix, SetMatrix method [XPS Documents and Packaging], SetMatrix method [XPS Documents and Packaging],IXpsOMMatrixTransform interface, xps.ixpsommatrixtransform_setmatrix, xpsobjectmodel/IXpsOMMatrixTransform::SetMatrix
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IXpsOMMatrixTransform::SetMatrix
 - xpsobjectmodel/IXpsOMMatrixTransform::SetMatrix
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMMatrixTransform.SetMatrix
---

# IXpsOMMatrixTransform::SetMatrix


## -description

Sets the <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_matrix">XPS_MATRIX</a> structure, which specifies the transform matrix.

## -parameters

### -param matrix [in]

The address of the <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_matrix">XPS_MATRIX</a> structure.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>.

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

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform">IXpsOMMatrixTransform</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_matrix">XPS_MATRIX</a>