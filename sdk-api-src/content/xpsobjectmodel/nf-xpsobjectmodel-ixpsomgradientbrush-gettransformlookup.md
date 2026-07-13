---
UID: NF:xpsobjectmodel.IXpsOMGradientBrush.GetTransformLookup
title: IXpsOMGradientBrush::GetTransformLookup (xpsobjectmodel.h)
description: Gets the name of the lookup key of the shared matrix transform interface that is to be used for the brush.
helpviewer_keywords: ["GetTransformLookup","GetTransformLookup method [XPS Documents and Packaging]","GetTransformLookup method [XPS Documents and Packaging]","IXpsOMGradientBrush interface","IXpsOMGradientBrush interface [XPS Documents and Packaging]","GetTransformLookup method","IXpsOMGradientBrush.GetTransformLookup","IXpsOMGradientBrush::GetTransformLookup","xps.ixpsomgradientbrush_gettransformlookup","xpsobjectmodel/IXpsOMGradientBrush::GetTransformLookup"]
old-location: xps\ixpsomgradientbrush_gettransformlookup.htm
tech.root: xps
ms.assetid: 60a91156-f9c8-4f6b-92b7-21e2fcd337fc
ms.date: 12/05/2018
ms.keywords: GetTransformLookup, GetTransformLookup method [XPS Documents and Packaging], GetTransformLookup method [XPS Documents and Packaging],IXpsOMGradientBrush interface, IXpsOMGradientBrush interface [XPS Documents and Packaging],GetTransformLookup method, IXpsOMGradientBrush.GetTransformLookup, IXpsOMGradientBrush::GetTransformLookup, xps.ixpsomgradientbrush_gettransformlookup, xpsobjectmodel/IXpsOMGradientBrush::GetTransformLookup
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
 - IXpsOMGradientBrush::GetTransformLookup
 - xpsobjectmodel/IXpsOMGradientBrush::GetTransformLookup
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
 - IXpsOMGradientBrush.GetTransformLookup
---

# IXpsOMGradientBrush::GetTransformLookup


## -description

Gets the name of the lookup key  of the shared matrix transform interface that is to be used for the brush.

The key name identifies a shared resource in a resource dictionary.

## -parameters

### -param key [out, retval]

The name of the lookup key  of the shared matrix transform interface that is to be used for the brush. If the lookup key name has not been set or if the local matrix transform has  been set, a <b>NULL</b> pointer is returned.

The value that is returned in this parameter depends on which method has been most recently called to set the lookup key or the transform.

<table>
<tr>
<th>Most recent method called</th>
<th>String that is returned in <i>key</i></th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgradientbrush-settransformlocal">SetTransformLocal</a>


</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgradientbrush-settransformlookup">SetTransformLookup</a>


</td>
<td>
The key that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgradientbrush-settransformlookup">SetTransformLookup</a>.

</td>
</tr>
<tr>
<td>
Neither <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgradientbrush-settransformlocal">SetTransformLocal</a> nor <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgradientbrush-settransformlookup">SetTransformLookup</a> has been called yet.

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

This method does not return an <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform">IXpsOMMatrixTransform</a> interface pointer; to retrieve this pointer  from the dictionary, call <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomdictionary-getbykey">IXpsOMDictionary::GetByKey</a>.

 The transform  determines how the gradient is transformed. The visible part of the gradient that is ultimately rendered in the image is determined by the path, stroke, or glyph that is using the gradient brush.

This method allocates the memory used by the string that is returned in <i>key</i>.  If <i>key</i> is not <b>NULL</b>, use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function  to free the memory.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdictionary">IXpsOMDictionary</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush">IXpsOMGradientBrush</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform">IXpsOMMatrixTransform</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>