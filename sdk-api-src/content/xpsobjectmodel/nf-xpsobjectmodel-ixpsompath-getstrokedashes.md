---
UID: NF:xpsobjectmodel.IXpsOMPath.GetStrokeDashes
title: IXpsOMPath::GetStrokeDashes (xpsobjectmodel.h)
description: Gets a pointer to the IXpsOMDashCollection interface that contains the XPS_DASH structures that define the dash pattern of the stroke.
helpviewer_keywords: ["GetStrokeDashes","GetStrokeDashes method [XPS Documents and Packaging]","GetStrokeDashes method [XPS Documents and Packaging]","IXpsOMPath interface","IXpsOMPath interface [XPS Documents and Packaging]","GetStrokeDashes method","IXpsOMPath.GetStrokeDashes","IXpsOMPath::GetStrokeDashes","xps.ixpsompath_getstrokedashes","xpsobjectmodel/IXpsOMPath::GetStrokeDashes"]
old-location: xps\ixpsompath_getstrokedashes.htm
tech.root: xps
ms.assetid: 60c76c8f-1434-4347-9639-a886d6ae133c
ms.date: 12/05/2018
ms.keywords: GetStrokeDashes, GetStrokeDashes method [XPS Documents and Packaging], GetStrokeDashes method [XPS Documents and Packaging],IXpsOMPath interface, IXpsOMPath interface [XPS Documents and Packaging],GetStrokeDashes method, IXpsOMPath.GetStrokeDashes, IXpsOMPath::GetStrokeDashes, xps.ixpsompath_getstrokedashes, xpsobjectmodel/IXpsOMPath::GetStrokeDashes
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
 - IXpsOMPath::GetStrokeDashes
 - xpsobjectmodel/IXpsOMPath::GetStrokeDashes
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
 - IXpsOMPath.GetStrokeDashes
---

# IXpsOMPath::GetStrokeDashes


## -description

Gets a pointer to the <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_dash">IXpsOMDashCollection</a> interface that contains the <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_dash">XPS_DASH</a> structures that  define the dash pattern of the stroke.

## -parameters

### -param strokeDashes [out, retval]

A pointer to the <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_dash">IXpsOMDashCollection</a> interface that contains the <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_dash">XPS_DASH</a> structures that  define the dash pattern of the stroke.

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
<i>strokeDashes</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection">IXpsOMDashCollection</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath">IXpsOMPath</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_dash">XPS_DASH</a>