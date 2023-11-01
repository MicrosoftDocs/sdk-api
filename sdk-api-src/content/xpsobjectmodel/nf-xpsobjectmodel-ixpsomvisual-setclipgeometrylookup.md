---
UID: NF:xpsobjectmodel.IXpsOMVisual.SetClipGeometryLookup
title: IXpsOMVisual::SetClipGeometryLookup (xpsobjectmodel.h)
description: Sets the lookup key name of a shared clip geometry in a resource dictionary.
helpviewer_keywords: ["IXpsOMVisual interface [XPS Documents and Packaging]","SetClipGeometryLookup method","IXpsOMVisual.SetClipGeometryLookup","IXpsOMVisual::SetClipGeometryLookup","SetClipGeometryLookup","SetClipGeometryLookup method [XPS Documents and Packaging]","SetClipGeometryLookup method [XPS Documents and Packaging]","IXpsOMVisual interface","xps.ixpsomvisual_setclipgeometrylookup","xpsobjectmodel/IXpsOMVisual::SetClipGeometryLookup"]
old-location: xps\ixpsomvisual_setclipgeometrylookup.htm
tech.root: xps
ms.assetid: 3f79f1ce-e761-44f7-970c-393c83f8f2fd
ms.date: 12/05/2018
ms.keywords: IXpsOMVisual interface [XPS Documents and Packaging],SetClipGeometryLookup method, IXpsOMVisual.SetClipGeometryLookup, IXpsOMVisual::SetClipGeometryLookup, SetClipGeometryLookup, SetClipGeometryLookup method [XPS Documents and Packaging], SetClipGeometryLookup method [XPS Documents and Packaging],IXpsOMVisual interface, xps.ixpsomvisual_setclipgeometrylookup, xpsobjectmodel/IXpsOMVisual::SetClipGeometryLookup
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
 - IXpsOMVisual::SetClipGeometryLookup
 - xpsobjectmodel/IXpsOMVisual::SetClipGeometryLookup
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
 - IXpsOMVisual.SetClipGeometryLookup
---

# IXpsOMVisual::SetClipGeometryLookup


## -description

Sets the lookup key name of a shared clip geometry in a resource dictionary.

## -parameters

### -param key [in]

The lookup key name of the clip geometry in the dictionary. A <b>NULL</b> pointer clears the previously assigned key name.

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

After you call <b>SetClipGeometryLookup</b>, the local clip geometry is released and <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-getclipgeometrylocal">GetClipGeometryLocal</a> returns a <b>NULL</b> pointer in the <i>clipGeometry</i> parameter. The table that follows explains the relationship between the local and lookup values of this property.


<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>clipGeometry</i>  by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-getclipgeometry">GetClipGeometry</a>
</th>
<th>Object that is returned in <i>clipGeometry</i>  by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-getclipgeometrylocal">GetClipGeometryLocal</a>
</th>
<th>String that is returned in <i>key</i>  by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-getclipgeometrylookup">GetClipGeometryLookup</a>
</th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setclipgeometrylocal">SetClipGeometryLocal</a>


</td>
<td>
The local clip geometry that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setclipgeometrylocal">SetClipGeometryLocal</a>.

</td>
<td>
The local clip geometry that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setclipgeometrylocal">SetClipGeometryLocal</a>.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>
<b>SetClipGeometryLookup</b> (this method)

</td>
<td>
The shared clip geometry that gets retrieved, with a lookup key that matches the key that is set by <b>SetClipGeometryLookup</b>, from the resource directory.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The lookup key that is set by <b>SetClipGeometryLookup</b>.

</td>
</tr>
<tr>
<td>
Neither <b>SetClipGeometryLookup</b> nor <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setclipgeometrylocal">SetClipGeometryLocal</a> has been called yet.

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

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>