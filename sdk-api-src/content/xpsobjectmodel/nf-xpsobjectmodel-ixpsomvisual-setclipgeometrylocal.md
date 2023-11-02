---
UID: NF:xpsobjectmodel.IXpsOMVisual.SetClipGeometryLocal
title: IXpsOMVisual::SetClipGeometryLocal (xpsobjectmodel.h)
description: Sets the local, unshared clipping region for the visual.
helpviewer_keywords: ["IXpsOMVisual interface [XPS Documents and Packaging]","SetClipGeometryLocal method","IXpsOMVisual.SetClipGeometryLocal","IXpsOMVisual::SetClipGeometryLocal","SetClipGeometryLocal","SetClipGeometryLocal method [XPS Documents and Packaging]","SetClipGeometryLocal method [XPS Documents and Packaging]","IXpsOMVisual interface","xps.ixpsomvisual_setclipgeometrylocal","xpsobjectmodel/IXpsOMVisual::SetClipGeometryLocal"]
old-location: xps\ixpsomvisual_setclipgeometrylocal.htm
tech.root: xps
ms.assetid: 8b703866-9dc0-4327-9988-908f17bd4b21
ms.date: 12/05/2018
ms.keywords: IXpsOMVisual interface [XPS Documents and Packaging],SetClipGeometryLocal method, IXpsOMVisual.SetClipGeometryLocal, IXpsOMVisual::SetClipGeometryLocal, SetClipGeometryLocal, SetClipGeometryLocal method [XPS Documents and Packaging], SetClipGeometryLocal method [XPS Documents and Packaging],IXpsOMVisual interface, xps.ixpsomvisual_setclipgeometrylocal, xpsobjectmodel/IXpsOMVisual::SetClipGeometryLocal
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
 - IXpsOMVisual::SetClipGeometryLocal
 - xpsobjectmodel/IXpsOMVisual::SetClipGeometryLocal
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
 - IXpsOMVisual.SetClipGeometryLocal
---

# IXpsOMVisual::SetClipGeometryLocal


## -description

Sets the local, unshared clipping region for the visual.

## -parameters

### -param clipGeometry [in]

A pointer to the  <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry">IXpsOMGeometry</a> interface to be set as the local, unshared clipping region for the visual. A <b>NULL</b> pointer releases the previously assigned geometry interface.

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
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>clipGeometry</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>

## -remarks

After you call <b>SetClipGeometryLocal</b>, the clip geometry lookup key is released and <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-getclipgeometrylookup">GetClipGeometryLookup</a> returns a <b>NULL</b> pointer in the <i>key</i> parameter. The table that follows explains the relationship between the local and lookup values of this property.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>clipGeometry</i>   by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-getclipgeometry">GetClipGeometry</a>
</th>
<th>Object that is returned in <i>clipGeometry</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-getclipgeometrylocal">GetClipGeometryLocal</a>
</th>
<th>String that is returned in <i>key</i>  by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-getclipgeometrylookup">GetClipGeometryLookup</a>
</th>
</tr>
<tr>
<td>
<b>SetClipGeometryLocal</b> (this method)

</td>
<td>
The local clip geometry that is set by <b>SetClipGeometryLocal</b>.

</td>
<td>
The local clip geometry that is set by <b>SetClipGeometryLocal</b>.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setclipgeometrylookup">SetClipGeometryLookup</a>


</td>
<td>
The shared clip geometry that gets retrieved, with a lookup key that matches the key that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setclipgeometrylookup">SetClipGeometryLookup</a>, from the resource directory.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The lookup key that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setclipgeometrylookup">SetClipGeometryLookup</a>.

</td>
</tr>
<tr>
<td>
Neither <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setclipgeometrylookup">SetClipGeometryLookup</a> nor <b>SetClipGeometryLocal</b> has been called yet.

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