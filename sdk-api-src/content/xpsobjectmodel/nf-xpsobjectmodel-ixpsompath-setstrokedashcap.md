---
UID: NF:xpsobjectmodel.IXpsOMPath.SetStrokeDashCap
title: IXpsOMPath::SetStrokeDashCap (xpsobjectmodel.h)
description: Sets the style of the stroke's dash cap.
helpviewer_keywords: ["IXpsOMPath interface [XPS Documents and Packaging]","SetStrokeDashCap method","IXpsOMPath.SetStrokeDashCap","IXpsOMPath::SetStrokeDashCap","SetStrokeDashCap","SetStrokeDashCap method [XPS Documents and Packaging]","SetStrokeDashCap method [XPS Documents and Packaging]","IXpsOMPath interface","xps.ixpsompath_setstrokedashcap","xpsobjectmodel/IXpsOMPath::SetStrokeDashCap"]
old-location: xps\ixpsompath_setstrokedashcap.htm
tech.root: xps
ms.assetid: 949f366b-1161-4db8-b9b9-d95b422b8931
ms.date: 12/05/2018
ms.keywords: IXpsOMPath interface [XPS Documents and Packaging],SetStrokeDashCap method, IXpsOMPath.SetStrokeDashCap, IXpsOMPath::SetStrokeDashCap, SetStrokeDashCap, SetStrokeDashCap method [XPS Documents and Packaging], SetStrokeDashCap method [XPS Documents and Packaging],IXpsOMPath interface, xps.ixpsompath_setstrokedashcap, xpsobjectmodel/IXpsOMPath::SetStrokeDashCap
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
 - IXpsOMPath::SetStrokeDashCap
 - xpsobjectmodel/IXpsOMPath::SetStrokeDashCap
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
 - IXpsOMPath.SetStrokeDashCap
---

# IXpsOMPath::SetStrokeDashCap


## -description

Sets the style of the stroke's dash cap.

## -parameters

### -param strokeDashCap [in]

The <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_dash_cap">XPS_DASH_CAP</a> value to be set.

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
<dt><b>E_INVALIDARG </b></dt>
</dl>
</td>
<td width="60%">
<i>strokeDashCap</i> was not a valid <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_dash_cap">XPS_DASH_CAP</a> value.

</td>
</tr>
</table>

## -remarks

For more information about dash cap styles, see <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_dash_cap">XPS_DASH_CAP</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath">IXpsOMPath</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_dash_cap">XPS_DASH_CAP</a>