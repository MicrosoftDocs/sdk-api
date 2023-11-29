---
UID: NF:xpsobjectmodel.IXpsOMGradientBrush.SetSpreadMethod
title: IXpsOMGradientBrush::SetSpreadMethod (xpsobjectmodel.h)
description: Sets the XPS_SPREAD_METHOD value, which describes how the area outside of the gradient region is to be rendered.
helpviewer_keywords: ["IXpsOMGradientBrush interface [XPS Documents and Packaging]","SetSpreadMethod method","IXpsOMGradientBrush.SetSpreadMethod","IXpsOMGradientBrush::SetSpreadMethod","SetSpreadMethod","SetSpreadMethod method [XPS Documents and Packaging]","SetSpreadMethod method [XPS Documents and Packaging]","IXpsOMGradientBrush interface","xps.ixpsomgradientbrush_setspreadmethod","xpsobjectmodel/IXpsOMGradientBrush::SetSpreadMethod"]
old-location: xps\ixpsomgradientbrush_setspreadmethod.htm
tech.root: xps
ms.assetid: 2114ba2e-95df-466e-983f-a56491bf891c
ms.date: 12/05/2018
ms.keywords: IXpsOMGradientBrush interface [XPS Documents and Packaging],SetSpreadMethod method, IXpsOMGradientBrush.SetSpreadMethod, IXpsOMGradientBrush::SetSpreadMethod, SetSpreadMethod, SetSpreadMethod method [XPS Documents and Packaging], SetSpreadMethod method [XPS Documents and Packaging],IXpsOMGradientBrush interface, xps.ixpsomgradientbrush_setspreadmethod, xpsobjectmodel/IXpsOMGradientBrush::SetSpreadMethod
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
 - IXpsOMGradientBrush::SetSpreadMethod
 - xpsobjectmodel/IXpsOMGradientBrush::SetSpreadMethod
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
 - IXpsOMGradientBrush.SetSpreadMethod
---

# IXpsOMGradientBrush::SetSpreadMethod


## -description

Sets the <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_spread_method">XPS_SPREAD_METHOD</a> value, which describes how the area outside of the gradient region is to be rendered.  The gradient region is defined by the start and end points of the gradient.

## -parameters

### -param spreadMethod [in]

The <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_spread_method">XPS_SPREAD_METHOD</a> value that describes how the area outside of the gradient region  is to be rendered. The gradient region is defined by the linear-gradient brush or radial-gradient brush that inherits this interface.

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
The <i>spreadMethod</i> parameter was not a valid <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_spread_method">XPS_SPREAD_METHOD</a> value.

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