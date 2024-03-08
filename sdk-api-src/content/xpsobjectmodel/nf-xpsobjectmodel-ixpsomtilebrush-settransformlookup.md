---
UID: NF:xpsobjectmodel.IXpsOMTileBrush.SetTransformLookup
title: IXpsOMTileBrush::SetTransformLookup (xpsobjectmodel.h)
description: Sets the lookup key name of a shared matrix transform that will be used as the transform for this brush.
helpviewer_keywords: ["IXpsOMTileBrush interface [XPS Documents and Packaging]","SetTransformLookup method","IXpsOMTileBrush.SetTransformLookup","IXpsOMTileBrush::SetTransformLookup","SetTransformLookup","SetTransformLookup method [XPS Documents and Packaging]","SetTransformLookup method [XPS Documents and Packaging]","IXpsOMTileBrush interface","xps.ixpsomtilebrush_settransformlookup","xpsobjectmodel/IXpsOMTileBrush::SetTransformLookup"]
old-location: xps\ixpsomtilebrush_settransformlookup.htm
tech.root: xps
ms.assetid: b2d9519a-9e22-44ba-839d-e1ba33aacc26
ms.date: 12/05/2018
ms.keywords: IXpsOMTileBrush interface [XPS Documents and Packaging],SetTransformLookup method, IXpsOMTileBrush.SetTransformLookup, IXpsOMTileBrush::SetTransformLookup, SetTransformLookup, SetTransformLookup method [XPS Documents and Packaging], SetTransformLookup method [XPS Documents and Packaging],IXpsOMTileBrush interface, xps.ixpsomtilebrush_settransformlookup, xpsobjectmodel/IXpsOMTileBrush::SetTransformLookup
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
 - IXpsOMTileBrush::SetTransformLookup
 - xpsobjectmodel/IXpsOMTileBrush::SetTransformLookup
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
 - IXpsOMTileBrush.SetTransformLookup
---

# IXpsOMTileBrush::SetTransformLookup


## -description

Sets the lookup key name of a shared matrix transform that will be used as the transform for this brush.The shared matrix transform that is referenced by the lookup key is stored in the resource dictionary.

## -parameters

### -param key [in]

A string variable that contains the lookup key name of a shared matrix transform in the resource dictionary. If a lookup key has already been set, a <b>NULL</b> pointer will clear it.

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
<dt><b>XPS_E_INVALID_RESOURCE_KEY</b></dt>
</dl>
</td>
<td width="60%">
According to the <a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>, the value of <i>lookup</i> is not a valid lookup key string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_INVALID_LOOKUP_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The lookup key name in <i>key</i> references an object that is not a geometry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_LOOKUP_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No object could be found with a key name that matched the value passed in <i>key</i>.

</td>
</tr>
</table>

## -remarks

The transform is applied before the brush image is rendered in the path, stroke, or glyph that is using the tile brush. The tile brush has only one transform, which can be local or remote.



After you call <b>SetTransformLookup</b>, the local transform is released and <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomtilebrush-gettransformlocal">GetTransformLocal</a> returns a <b>NULL</b> pointer in the <i>transform</i> parameter. The table that follows explains the relationship between the local and lookup values of this property.


<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned  in <i>transform</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomtilebrush-gettransform">GetTransform</a>
</th>
<th>Object that is returned  in <i>transform</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomtilebrush-gettransformlocal">GetTransformLocal</a>
</th>
<th>String that is returned  in <i>key</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomtilebrush-gettransformlookup">GetTransformLookup</a>
</th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomtilebrush-settransformlocal">SetTransformLocal</a>


</td>
<td>
The transform that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomtilebrush-settransformlocal">SetTransformLocal</a>.

</td>
<td>
The transform that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomtilebrush-settransformlocal">SetTransformLocal</a>.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>
<b>SetTransformLookup</b> (this method)

</td>
<td>
The transform which is retrieved—using a lookup key that matches the key that is set by <b>SetTransformLookup</b>— from the resource directory.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The lookup key that is set by <b>SetTransformLookup</b>.

</td>
</tr>
<tr>
<td>
Neither <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomtilebrush-settransformlocal">SetTransformLocal</a> nor <b>SetTransformLookup</b> has been called yet.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush">IXpsOMTileBrush</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>