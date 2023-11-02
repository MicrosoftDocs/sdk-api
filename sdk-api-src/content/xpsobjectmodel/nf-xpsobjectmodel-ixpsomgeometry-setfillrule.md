---
UID: NF:xpsobjectmodel.IXpsOMGeometry.SetFillRule
title: IXpsOMGeometry::SetFillRule (xpsobjectmodel.h)
description: Sets the XPS_FILL_RULE value that describes the fill rule to be used.
helpviewer_keywords: ["IXpsOMGeometry interface [XPS Documents and Packaging]","SetFillRule method","IXpsOMGeometry.SetFillRule","IXpsOMGeometry::SetFillRule","SetFillRule","SetFillRule method [XPS Documents and Packaging]","SetFillRule method [XPS Documents and Packaging]","IXpsOMGeometry interface","xps.ixpsomgeometry_setfillrule","xpsobjectmodel/IXpsOMGeometry::SetFillRule"]
old-location: xps\ixpsomgeometry_setfillrule.htm
tech.root: xps
ms.assetid: e219a505-48e0-46b0-a739-d46fb898bc58
ms.date: 12/05/2018
ms.keywords: IXpsOMGeometry interface [XPS Documents and Packaging],SetFillRule method, IXpsOMGeometry.SetFillRule, IXpsOMGeometry::SetFillRule, SetFillRule, SetFillRule method [XPS Documents and Packaging], SetFillRule method [XPS Documents and Packaging],IXpsOMGeometry interface, xps.ixpsomgeometry_setfillrule, xpsobjectmodel/IXpsOMGeometry::SetFillRule
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
 - IXpsOMGeometry::SetFillRule
 - xpsobjectmodel/IXpsOMGeometry::SetFillRule
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
 - IXpsOMGeometry.SetFillRule
---

# IXpsOMGeometry::SetFillRule


## -description

Sets the  <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_fill_rule">XPS_FILL_RULE</a> value that describes the fill rule to be used.

## -parameters

### -param fillRule [in]

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>fillRule</i> is not a valid <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_fill_rule">XPS_FILL_RULE</a> value.

</td>
</tr>
</table>

## -remarks

For more information about how the file rule determines whether a point is inside the fill region, see <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_fill_rule">XPS_FILL_RULE</a>. 

In the document markup, this value corresponds to the <b>FillRule</b> attribute of the <b>PathGeometry</b> element.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry">IXpsOMGeometry</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_fill_rule">XPS_FILL_RULE</a>