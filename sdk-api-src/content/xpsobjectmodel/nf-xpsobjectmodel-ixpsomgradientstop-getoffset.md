---
UID: NF:xpsobjectmodel.IXpsOMGradientStop.GetOffset
title: IXpsOMGradientStop::GetOffset (xpsobjectmodel.h)
description: Gets the offset value of the gradient stop.
helpviewer_keywords: ["GetOffset","GetOffset method [XPS Documents and Packaging]","GetOffset method [XPS Documents and Packaging]","IXpsOMGradientStop interface","IXpsOMGradientStop interface [XPS Documents and Packaging]","GetOffset method","IXpsOMGradientStop.GetOffset","IXpsOMGradientStop::GetOffset","xps.ixpsomgradientstop_getoffset","xpsobjectmodel/IXpsOMGradientStop::GetOffset"]
old-location: xps\ixpsomgradientstop_getoffset.htm
tech.root: xps
ms.assetid: 14048707-1a73-40a1-9094-da4885d9934d
ms.date: 12/05/2018
ms.keywords: GetOffset, GetOffset method [XPS Documents and Packaging], GetOffset method [XPS Documents and Packaging],IXpsOMGradientStop interface, IXpsOMGradientStop interface [XPS Documents and Packaging],GetOffset method, IXpsOMGradientStop.GetOffset, IXpsOMGradientStop::GetOffset, xps.ixpsomgradientstop_getoffset, xpsobjectmodel/IXpsOMGradientStop::GetOffset
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
 - IXpsOMGradientStop::GetOffset
 - xpsobjectmodel/IXpsOMGradientStop::GetOffset
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
 - IXpsOMGradientStop.GetOffset
---

# IXpsOMGradientStop::GetOffset


## -description

Gets the offset value of the gradient stop.

## -parameters

### -param offset [out, retval]

The offset value of the gradient stop, expressed as a fraction of the gradient path.

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
<i>offset</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The valid range of  values returned in <i>offset</i> is 0.0–1.0. 0.0 is the start point of the gradient, 1.0 is the end point, and a value between 0.0 and 1.0 is a location that is linearly interpolated between the start point and the end point.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop">IXpsOMGradientStop</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>