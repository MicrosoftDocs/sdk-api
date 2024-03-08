---
UID: NF:xpsobjectmodel.IXpsOMGradientStop.SetColor
title: IXpsOMGradientStop::SetColor (xpsobjectmodel.h)
description: Sets the color value and color profile of the gradient stop.
helpviewer_keywords: ["IXpsOMGradientStop interface [XPS Documents and Packaging]","SetColor method","IXpsOMGradientStop.SetColor","IXpsOMGradientStop::SetColor","SetColor","SetColor method [XPS Documents and Packaging]","SetColor method [XPS Documents and Packaging]","IXpsOMGradientStop interface","xps.ixpsomgradientstop_setcolor","xpsobjectmodel/IXpsOMGradientStop::SetColor"]
old-location: xps\ixpsomgradientstop_setcolor.htm
tech.root: xps
ms.assetid: 535b14f3-6d17-4c3c-b310-b018922d48e8
ms.date: 12/05/2018
ms.keywords: IXpsOMGradientStop interface [XPS Documents and Packaging],SetColor method, IXpsOMGradientStop.SetColor, IXpsOMGradientStop::SetColor, SetColor, SetColor method [XPS Documents and Packaging], SetColor method [XPS Documents and Packaging],IXpsOMGradientStop interface, xps.ixpsomgradientstop_setcolor, xpsobjectmodel/IXpsOMGradientStop::SetColor
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
 - IXpsOMGradientStop::SetColor
 - xpsobjectmodel/IXpsOMGradientStop::SetColor
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
 - IXpsOMGradientStop.SetColor
---

# IXpsOMGradientStop::SetColor


## -description

Sets the color value and color profile of the gradient stop.

## -parameters

### -param color [in]

The color value to be set at the gradient stop.

If the value of the <b>colorType</b> field in the <a href="/previous-versions/windows/desktop/dd372939(v=vs.85)">XPS_COLOR</a> structure that is passed in this parameter is <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_color_type">XPS_COLOR_TYPE_CONTEXT</a>, a valid color profile must be provided in the <i>colorProfile</i> parameter.

### -param colorProfile [in]

The color profile to be used with <i>color</i>.

A color profile is required when the value of the <b>colorType</b> field in the <a href="/previous-versions/windows/desktop/dd372939(v=vs.85)">XPS_COLOR</a> structure that is passed  in the <i>color</i> parameter is <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_color_type">XPS_COLOR_TYPE_CONTEXT</a>. If the value of the <b>colorType</b> field is not <b>XPS_COLOR_TYPE_CONTEXT</b>, this parameter must be set to <b>NULL</b>.

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
<i>color</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_MISSING_COLORPROFILE</b></dt>
</dl>
</td>
<td width="60%">
<i>colorProfile</i> is <b>NULL</b> when a color profile was expected. A color profile is required when the color type is <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_color_type">XPS_COLOR_TYPE_CONTEXT</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>colorProfile</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_UNEXPECTED_COLORPROFILE</b></dt>
</dl>
</td>
<td width="60%">
<i>colorProfile</i> contained a color profile when one was not expected. A color profile is only allowed when the color type is <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_color_type">XPS_COLOR_TYPE_CONTEXT</a>.

</td>
</tr>
</table>

## -remarks

A color profile is only required when the color type of <i>color</i> is <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_color_type">XPS_COLOR_TYPE_CONTEXT</a>.

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresource">IXpsOMColorProfileResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop">IXpsOMGradientStop</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/previous-versions/windows/desktop/dd372939(v=vs.85)">XPS_COLOR</a>