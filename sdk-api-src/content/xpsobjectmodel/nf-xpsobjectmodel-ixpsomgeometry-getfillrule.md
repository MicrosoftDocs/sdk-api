---
UID: NF:xpsobjectmodel.IXpsOMGeometry.GetFillRule
title: IXpsOMGeometry::GetFillRule (xpsobjectmodel.h)
description: Gets the XPS_FILL_RULE value that describes the fill rule to be used.
helpviewer_keywords: ["GetFillRule","GetFillRule method [XPS Documents and Packaging]","GetFillRule method [XPS Documents and Packaging]","IXpsOMGeometry interface","IXpsOMGeometry interface [XPS Documents and Packaging]","GetFillRule method","IXpsOMGeometry.GetFillRule","IXpsOMGeometry::GetFillRule","xps.ixpsomgeometry_getfillrule","xpsobjectmodel/IXpsOMGeometry::GetFillRule"]
old-location: xps\ixpsomgeometry_getfillrule.htm
tech.root: xps
ms.assetid: 5ec2cfdd-f05d-4e05-b290-fad175fe1cae
ms.date: 12/05/2018
ms.keywords: GetFillRule, GetFillRule method [XPS Documents and Packaging], GetFillRule method [XPS Documents and Packaging],IXpsOMGeometry interface, IXpsOMGeometry interface [XPS Documents and Packaging],GetFillRule method, IXpsOMGeometry.GetFillRule, IXpsOMGeometry::GetFillRule, xps.ixpsomgeometry_getfillrule, xpsobjectmodel/IXpsOMGeometry::GetFillRule
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
 - IXpsOMGeometry::GetFillRule
 - xpsobjectmodel/IXpsOMGeometry::GetFillRule
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
 - IXpsOMGeometry.GetFillRule
---

# IXpsOMGeometry::GetFillRule


## -description

Gets the  <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_fill_rule">XPS_FILL_RULE</a> value that describes the fill rule to be used.

## -parameters

### -param fillRule [out, retval]

The <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_fill_rule">XPS_FILL_RULE</a> value that describes the fill rule to be used.

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
<i>fillRule</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

For more information about how the file rule determines whether a point is inside the fill region, see <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_fill_rule">XPS_FILL_RULE</a>. 

The value that is returned in <i>fillRule</i>  corresponds to the <b>FillRule</b> attribute of the <b>PathGeometry</b> element in the document markup.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry">IXpsOMGeometry</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_fill_rule">XPS_FILL_RULE</a>