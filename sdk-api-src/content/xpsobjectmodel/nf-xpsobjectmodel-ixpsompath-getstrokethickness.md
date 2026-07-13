---
UID: NF:xpsobjectmodel.IXpsOMPath.GetStrokeThickness
title: IXpsOMPath::GetStrokeThickness (xpsobjectmodel.h)
description: Gets the stroke thickness.
helpviewer_keywords: ["GetStrokeThickness","GetStrokeThickness method [XPS Documents and Packaging]","GetStrokeThickness method [XPS Documents and Packaging]","IXpsOMPath interface","IXpsOMPath interface [XPS Documents and Packaging]","GetStrokeThickness method","IXpsOMPath.GetStrokeThickness","IXpsOMPath::GetStrokeThickness","xps.ixpsompath_getstrokethickness","xpsobjectmodel/IXpsOMPath::GetStrokeThickness"]
old-location: xps\ixpsompath_getstrokethickness.htm
tech.root: xps
ms.assetid: 5c1d8179-99e6-4335-8777-56b6873f746b
ms.date: 12/05/2018
ms.keywords: GetStrokeThickness, GetStrokeThickness method [XPS Documents and Packaging], GetStrokeThickness method [XPS Documents and Packaging],IXpsOMPath interface, IXpsOMPath interface [XPS Documents and Packaging],GetStrokeThickness method, IXpsOMPath.GetStrokeThickness, IXpsOMPath::GetStrokeThickness, xps.ixpsompath_getstrokethickness, xpsobjectmodel/IXpsOMPath::GetStrokeThickness
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
 - IXpsOMPath::GetStrokeThickness
 - xpsobjectmodel/IXpsOMPath::GetStrokeThickness
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
 - IXpsOMPath.GetStrokeThickness
---

# IXpsOMPath::GetStrokeThickness


## -description

Gets the stroke thickness.

## -parameters

### -param strokeThickness [out, retval]

The stroke thickness value.

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
<i>strokeStartLineCap</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The value returned in <i>strokeThickness</i> specifies the thickness of a stroke in units of the effective coordinate space. The units include the path's render transform.

The stroke is drawn on top of the boundary of the path's geometry, such that one half of the stroke's width extends outside of the path's specified geometry  and the other half falls inside of it.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath">IXpsOMPath</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>