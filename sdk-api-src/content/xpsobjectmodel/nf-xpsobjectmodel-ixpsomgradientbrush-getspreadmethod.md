---
UID: NF:xpsobjectmodel.IXpsOMGradientBrush.GetSpreadMethod
title: IXpsOMGradientBrush::GetSpreadMethod (xpsobjectmodel.h)
description: Gets the XPS_SPREAD_METHOD value, which describes how the area outside of the gradient region will be rendered.
helpviewer_keywords: ["GetSpreadMethod","GetSpreadMethod method [XPS Documents and Packaging]","GetSpreadMethod method [XPS Documents and Packaging]","IXpsOMGradientBrush interface","IXpsOMGradientBrush interface [XPS Documents and Packaging]","GetSpreadMethod method","IXpsOMGradientBrush.GetSpreadMethod","IXpsOMGradientBrush::GetSpreadMethod","xps.ixpsomgradientbrush_getspreadmethod","xpsobjectmodel/IXpsOMGradientBrush::GetSpreadMethod"]
old-location: xps\ixpsomgradientbrush_getspreadmethod.htm
tech.root: xps
ms.assetid: c4c62817-735b-4ef1-84cf-1c9fa63f55ee
ms.date: 12/05/2018
ms.keywords: GetSpreadMethod, GetSpreadMethod method [XPS Documents and Packaging], GetSpreadMethod method [XPS Documents and Packaging],IXpsOMGradientBrush interface, IXpsOMGradientBrush interface [XPS Documents and Packaging],GetSpreadMethod method, IXpsOMGradientBrush.GetSpreadMethod, IXpsOMGradientBrush::GetSpreadMethod, xps.ixpsomgradientbrush_getspreadmethod, xpsobjectmodel/IXpsOMGradientBrush::GetSpreadMethod
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
 - IXpsOMGradientBrush::GetSpreadMethod
 - xpsobjectmodel/IXpsOMGradientBrush::GetSpreadMethod
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
 - IXpsOMGradientBrush.GetSpreadMethod
---

# IXpsOMGradientBrush::GetSpreadMethod


## -description

Gets the <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_spread_method">XPS_SPREAD_METHOD</a> value, which describes how the area outside of the gradient region will be rendered.

## -parameters

### -param spreadMethod [out, retval]

The <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_spread_method">XPS_SPREAD_METHOD</a> value that describes how the area outside of the gradient region will be rendered. The gradient region is defined by the linear-gradient brush or radial-gradient brush that inherits this interface.

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
<i>spreadMethod</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

For more information about different types of spread methods, see <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_spread_method">XPS_SPREAD_METHOD</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush">IXpsOMGradientBrush</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush">IXpsOMLinearGradientBrush</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush">IXpsOMRadialGradientBrush</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_spread_method">XPS_SPREAD_METHOD</a>