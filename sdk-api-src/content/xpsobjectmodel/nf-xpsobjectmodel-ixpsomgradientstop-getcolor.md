---
UID: NF:xpsobjectmodel.IXpsOMGradientStop.GetColor
title: IXpsOMGradientStop::GetColor (xpsobjectmodel.h)
description: Gets the color value and color profile of the gradient stop.
helpviewer_keywords: ["GetColor","GetColor method [XPS Documents and Packaging]","GetColor method [XPS Documents and Packaging]","IXpsOMGradientStop interface","IXpsOMGradientStop interface [XPS Documents and Packaging]","GetColor method","IXpsOMGradientStop.GetColor","IXpsOMGradientStop::GetColor","xps.ixpsomgradientstop_getcolor","xpsobjectmodel/IXpsOMGradientStop::GetColor"]
old-location: xps\ixpsomgradientstop_getcolor.htm
tech.root: xps
ms.assetid: 6630d58f-d0f0-4b39-a14c-d3955f0f401a
ms.date: 12/05/2018
ms.keywords: GetColor, GetColor method [XPS Documents and Packaging], GetColor method [XPS Documents and Packaging],IXpsOMGradientStop interface, IXpsOMGradientStop interface [XPS Documents and Packaging],GetColor method, IXpsOMGradientStop.GetColor, IXpsOMGradientStop::GetColor, xps.ixpsomgradientstop_getcolor, xpsobjectmodel/IXpsOMGradientStop::GetColor
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
 - IXpsOMGradientStop::GetColor
 - xpsobjectmodel/IXpsOMGradientStop::GetColor
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
 - IXpsOMGradientStop.GetColor
---

# IXpsOMGradientStop::GetColor


## -description

Gets the color value and color profile of the gradient stop.

## -parameters

### -param color [out]

The color value of the gradient stop.

### -param colorProfile [out, retval]

A pointer to the <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresource">IXpsOMColorProfileResource</a> interface that contains the color profile to be used. If no color profile resource has been set, a <b>NULL</b> pointer is returned. See remarks.

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
<i>color</i>,  <i>colorProfile</i>, or both were <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

A color profile is only returned when the color type of <i>color</i> is <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_color_type">XPS_COLOR_TYPE_CONTEXT</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresource">IXpsOMColorProfileResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop">IXpsOMGradientStop</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/previous-versions/windows/desktop/dd372939(v=vs.85)">XPS_COLOR</a>