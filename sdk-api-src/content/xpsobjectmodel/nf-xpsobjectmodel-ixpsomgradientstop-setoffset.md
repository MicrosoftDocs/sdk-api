---
UID: NF:xpsobjectmodel.IXpsOMGradientStop.SetOffset
title: IXpsOMGradientStop::SetOffset (xpsobjectmodel.h)
description: Sets the offset location of the gradient stop.
helpviewer_keywords: ["IXpsOMGradientStop interface [XPS Documents and Packaging]","SetOffset method","IXpsOMGradientStop.SetOffset","IXpsOMGradientStop::SetOffset","SetOffset","SetOffset method [XPS Documents and Packaging]","SetOffset method [XPS Documents and Packaging]","IXpsOMGradientStop interface","xps.ixpsomgradientstop_setoffset","xpsobjectmodel/IXpsOMGradientStop::SetOffset"]
old-location: xps\ixpsomgradientstop_setoffset.htm
tech.root: xps
ms.assetid: 8c1932b0-386b-4779-a4e4-e239e42e1d16
ms.date: 12/05/2018
ms.keywords: IXpsOMGradientStop interface [XPS Documents and Packaging],SetOffset method, IXpsOMGradientStop.SetOffset, IXpsOMGradientStop::SetOffset, SetOffset, SetOffset method [XPS Documents and Packaging], SetOffset method [XPS Documents and Packaging],IXpsOMGradientStop interface, xps.ixpsomgradientstop_setoffset, xpsobjectmodel/IXpsOMGradientStop::SetOffset
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
 - IXpsOMGradientStop::SetOffset
 - xpsobjectmodel/IXpsOMGradientStop::SetOffset
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
 - IXpsOMGradientStop.SetOffset
---

# IXpsOMGradientStop::SetOffset


## -description

Sets the offset location of the gradient stop.

## -parameters

### -param offset [in]

The offset value that describes the location of the gradient stop as a fraction of the gradient path.

The valid range of this parameter is 0.0 &lt;= <i>offset</i> &lt;= 1.0.

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
<i>offset</i> did not contain a valid offset value.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop">IXpsOMGradientStop</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>