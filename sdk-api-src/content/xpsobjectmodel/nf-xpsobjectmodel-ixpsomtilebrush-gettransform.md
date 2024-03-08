---
UID: NF:xpsobjectmodel.IXpsOMTileBrush.GetTransform
title: IXpsOMTileBrush::GetTransform (xpsobjectmodel.h)
description: Gets a pointer to the IXpsOMMatrixTransform interface that contains the resolved matrix transform for the brush. (IXpsOMTileBrush.GetTransform)
helpviewer_keywords: ["GetTransform","GetTransform method [XPS Documents and Packaging]","GetTransform method [XPS Documents and Packaging]","IXpsOMTileBrush interface","IXpsOMTileBrush interface [XPS Documents and Packaging]","GetTransform method","IXpsOMTileBrush.GetTransform","IXpsOMTileBrush::GetTransform","xps.ixpsomtilebrush_gettransform","xpsobjectmodel/IXpsOMTileBrush::GetTransform"]
old-location: xps\ixpsomtilebrush_gettransform.htm
tech.root: xps
ms.assetid: db4c4ef8-d5f4-4cff-b38d-d211e14a98c1
ms.date: 12/05/2018
ms.keywords: GetTransform, GetTransform method [XPS Documents and Packaging], GetTransform method [XPS Documents and Packaging],IXpsOMTileBrush interface, IXpsOMTileBrush interface [XPS Documents and Packaging],GetTransform method, IXpsOMTileBrush.GetTransform, IXpsOMTileBrush::GetTransform, xps.ixpsomtilebrush_gettransform, xpsobjectmodel/IXpsOMTileBrush::GetTransform
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
 - IXpsOMTileBrush::GetTransform
 - xpsobjectmodel/IXpsOMTileBrush::GetTransform
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
 - IXpsOMTileBrush.GetTransform
---

# IXpsOMTileBrush::GetTransform


## -description

Gets a pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform">IXpsOMMatrixTransform</a> interface that contains the resolved matrix transform for the brush.

## -parameters

### -param transform [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform">IXpsOMMatrixTransform</a>  interface that contains the resolved matrix transform for the brush. If a matrix transform has not been set, a <b>NULL</b> pointer is returned.

The value that is returned in this parameter depends on which method has most recently been called to set the transform.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned  in <i>transform</i></th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomtilebrush-settransformlocal">SetTransformLocal</a>


</td>
<td>
The transform that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomtilebrush-settransformlocal">SetTransformLocal</a>.

</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomtilebrush-settransformlookup">SetTransformLookup</a>


</td>
<td>
The transform which is retrieved, using a lookup key that matches the key that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomtilebrush-settransformlookup">SetTransformLookup</a>, from the resource directory.

</td>
</tr>
<tr>
<td>
Neither <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomtilebrush-settransformlocal">SetTransformLocal</a> nor <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomtilebrush-settransformlookup">SetTransformLookup</a> has been called yet.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
</table>

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
<i>transform</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_LOOKUP_INVALID_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The lookup key name set by  <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup">SetStrokeBrushLookup</a> references an object that is not a brush.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_LOOKUP_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No object could be found with a key name that matched the lookup value.

</td>
</tr>
</table>

## -remarks

The transform determines how the output area is transformed before the brush image is rendered in the path, stroke, or glyph that is using the tile brush.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform">IXpsOMMatrixTransform</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush">IXpsOMTileBrush</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>
