---
UID: NF:xpsobjectmodel.IXpsOMVisual.GetClipGeometryLookup
title: IXpsOMVisual::GetClipGeometryLookup (xpsobjectmodel.h)
description: Gets the lookup key for the IXpsOMGeometry interface in a resource dictionary that contains the visual's clipping region.
helpviewer_keywords: ["GetClipGeometryLookup","GetClipGeometryLookup method [XPS Documents and Packaging]","GetClipGeometryLookup method [XPS Documents and Packaging]","IXpsOMVisual interface","IXpsOMVisual interface [XPS Documents and Packaging]","GetClipGeometryLookup method","IXpsOMVisual.GetClipGeometryLookup","IXpsOMVisual::GetClipGeometryLookup","xps.ixpsomvisual_getclipgeometrylookup","xpsobjectmodel/IXpsOMVisual::GetClipGeometryLookup"]
old-location: xps\ixpsomvisual_getclipgeometrylookup.htm
tech.root: xps
ms.assetid: aa101ac6-65e8-4f6b-a6fa-59f3a003ffc5
ms.date: 12/05/2018
ms.keywords: GetClipGeometryLookup, GetClipGeometryLookup method [XPS Documents and Packaging], GetClipGeometryLookup method [XPS Documents and Packaging],IXpsOMVisual interface, IXpsOMVisual interface [XPS Documents and Packaging],GetClipGeometryLookup method, IXpsOMVisual.GetClipGeometryLookup, IXpsOMVisual::GetClipGeometryLookup, xps.ixpsomvisual_getclipgeometrylookup, xpsobjectmodel/IXpsOMVisual::GetClipGeometryLookup
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
 - IXpsOMVisual::GetClipGeometryLookup
 - xpsobjectmodel/IXpsOMVisual::GetClipGeometryLookup
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
 - IXpsOMVisual.GetClipGeometryLookup
---

# IXpsOMVisual::GetClipGeometryLookup


## -description

Gets the lookup key for the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry">IXpsOMGeometry</a> interface in a resource dictionary that contains the visual's clipping region.

## -parameters

### -param key [out, retval]

The lookup key for the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry">IXpsOMGeometry</a> interface in a resource dictionary that contains the visual's clipping region. If a lookup key for the  clip geometry  has not been set, or if a local clip geometry has  been set, a <b>NULL</b> pointer is returned.

<table>
<tr>
<th>Most recent method called</th>
<th>Lookup key string that is returned in <i>key</i></th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setclipgeometrylocal">SetClipGeometryLocal</a>


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
The lookup key that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setclipgeometrylookup">SetClipGeometryLookup</a>.

</td>
</tr>
<tr>
<td>
Neither <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setclipgeometrylocal">SetClipGeometryLocal</a> nor <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomvisual-setclipgeometrylookup">SetClipGeometryLookup</a> has been called yet.

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

This method allocates the memory that is used by the string returned in <i>key</i>.  If <i>key</i> is not <b>NULL</b>, use the  SignatureDefinitions   function to free the memory.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry">IXpsOMGeometry</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisual">IXpsOMVisual</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>