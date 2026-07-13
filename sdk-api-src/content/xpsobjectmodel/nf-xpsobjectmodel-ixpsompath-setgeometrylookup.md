---
UID: NF:xpsobjectmodel.IXpsOMPath.SetGeometryLookup
title: IXpsOMPath::SetGeometryLookup (xpsobjectmodel.h)
description: Sets the lookup key name of a shared geometry in a resource dictionary.
helpviewer_keywords: ["IXpsOMPath interface [XPS Documents and Packaging]","SetGeometryLookup method","IXpsOMPath.SetGeometryLookup","IXpsOMPath::SetGeometryLookup","SetGeometryLookup","SetGeometryLookup method [XPS Documents and Packaging]","SetGeometryLookup method [XPS Documents and Packaging]","IXpsOMPath interface","xps.ixpsompath_setgeometrylookup","xpsobjectmodel/IXpsOMPath::SetGeometryLookup"]
old-location: xps\ixpsompath_setgeometrylookup.htm
tech.root: xps
ms.assetid: 7a60bf60-e69b-4a8a-94e9-5d304aa25dd5
ms.date: 12/05/2018
ms.keywords: IXpsOMPath interface [XPS Documents and Packaging],SetGeometryLookup method, IXpsOMPath.SetGeometryLookup, IXpsOMPath::SetGeometryLookup, SetGeometryLookup, SetGeometryLookup method [XPS Documents and Packaging], SetGeometryLookup method [XPS Documents and Packaging],IXpsOMPath interface, xps.ixpsompath_setgeometrylookup, xpsobjectmodel/IXpsOMPath::SetGeometryLookup
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
 - IXpsOMPath::SetGeometryLookup
 - xpsobjectmodel/IXpsOMPath::SetGeometryLookup
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
 - IXpsOMPath.SetGeometryLookup
---

# IXpsOMPath::SetGeometryLookup


## -description

Sets the lookup key name of a shared geometry in a resource dictionary. 

Here, the  geometry describes the resolved fill area to be set for this path.

## -parameters

### -param lookup [in]

The lookup key name of a shared geometry in a resource dictionary.

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
The lookup key name in <i>lookup</i> references an object that is not a geometry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_LOOKUP_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No object could be found with a key name that matched the value passed in <i>lookup</i>.

</td>
</tr>
</table>

## -remarks

After you call <b>SetGeometryLookup</b>, the local geometry is released and <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setgeometrylocal">SetGeometryLocal</a> returns a <b>NULL</b> pointer in the <i>geometry</i> parameter. The table that follows explains the relationship between the local and lookup values of this property.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>geometry</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getgeometry">GetGeometry</a>
</th>
<th>Object that is returned in <i>geometry</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getgeometrylocal">GetGeometryLocal</a>
</th>
<th>String that is returned in <i>lookup</i> by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getgeometrylookup">GetGeometryLookup</a>
</th>
</tr>
<tr>
<td>

<a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setgeometrylocal">SetGeometryLocal</a>


</td>
<td>
The local geometry that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setgeometrylocal">SetGeometryLocal</a>.

</td>
<td>
The local geometry that is set by <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setgeometrylocal">SetGeometryLocal</a>.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>
<b>SetGeometryLookup</b> (this method)

</td>
<td>
The shared geometry retrieved, with a lookup key that matches the key that is set by <b>SetGeometryLookup</b>, from the resource directory.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The lookup key that is set by <b>SetGeometryLookup</b>.

</td>
</tr>
<tr>
<td>
Neither <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setgeometrylocal">SetGeometryLocal</a> nor <b>SetGeometryLookup</b> has been called yet.

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

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath">IXpsOMPath</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>