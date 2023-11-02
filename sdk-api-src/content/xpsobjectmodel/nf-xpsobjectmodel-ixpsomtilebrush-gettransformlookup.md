---
UID: NF:xpsobjectmodel.IXpsOMTileBrush.GetTransformLookup
title: IXpsOMTileBrush::GetTransformLookup (xpsobjectmodel.h)
description: Gets the lookup key that identifies the IXpsOMMatrixTransform interface in a resource dictionary that contains the resolved matrix transform for the brush.
helpviewer_keywords: ["GetTransformLookup","GetTransformLookup method [XPS Documents and Packaging]","GetTransformLookup method [XPS Documents and Packaging]","IXpsOMTileBrush interface","IXpsOMTileBrush interface [XPS Documents and Packaging]","GetTransformLookup method","IXpsOMTileBrush.GetTransformLookup","IXpsOMTileBrush::GetTransformLookup","xps.ixpsomtilebrush_gettransformlookup","xpsobjectmodel/IXpsOMTileBrush::GetTransformLookup"]
old-location: xps\ixpsomtilebrush_gettransformlookup.htm
tech.root: xps
ms.assetid: bebed09b-7af7-4da1-aaa3-e8e2a45f2717
ms.date: 12/05/2018
ms.keywords: GetTransformLookup, GetTransformLookup method [XPS Documents and Packaging], GetTransformLookup method [XPS Documents and Packaging],IXpsOMTileBrush interface, IXpsOMTileBrush interface [XPS Documents and Packaging],GetTransformLookup method, IXpsOMTileBrush.GetTransformLookup, IXpsOMTileBrush::GetTransformLookup, xps.ixpsomtilebrush_gettransformlookup, xpsobjectmodel/IXpsOMTileBrush::GetTransformLookup
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
 - IXpsOMTileBrush::GetTransformLookup
 - xpsobjectmodel/IXpsOMTileBrush::GetTransformLookup
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
 - IXpsOMTileBrush.GetTransformLookup
---

# IXpsOMTileBrush::GetTransformLookup


## -description

Gets the lookup key that identifies the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform">IXpsOMMatrixTransform</a> interface in a resource dictionary that contains the resolved matrix transform for the brush.

## -parameters

### -param key [out, retval]

The lookup key that identifies the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform">IXpsOMMatrixTransform</a> interface in a resource dictionary that contains the resolved matrix transform for the brush. If a matrix transform lookup key has not been set or if a local matrix transform has  been set, a <b>NULL</b> pointer is returned.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned  in <i>key</i></th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomtilebrush-settransformlocal">SetTransformLocal</a>


</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomtilebrush-settransformlookup">SetTransformLookup</a>


</td>
<td>
The lookup key  set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomtilebrush-settransformlookup">SetTransformLookup</a>.

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
<i>key</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The transform determines how the output area is transformed before the brush image is rendered in the path, stroke, or glyph that is using the tile brush.

This method allocates the memory used by the string that is returned in <i>key</i>.  If <i>key</i> is not <b>NULL</b>, use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform">IXpsOMMatrixTransform</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush">IXpsOMTileBrush</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>