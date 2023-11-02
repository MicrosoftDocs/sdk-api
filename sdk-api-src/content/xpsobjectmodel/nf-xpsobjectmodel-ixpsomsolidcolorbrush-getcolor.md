---
UID: NF:xpsobjectmodel.IXpsOMSolidColorBrush.GetColor
title: IXpsOMSolidColorBrush::GetColor (xpsobjectmodel.h)
description: Gets the color value and color profile of the brush.
helpviewer_keywords: ["GetColor","GetColor method [XPS Documents and Packaging]","GetColor method [XPS Documents and Packaging]","IXpsOMSolidColorBrush interface","IXpsOMSolidColorBrush interface [XPS Documents and Packaging]","GetColor method","IXpsOMSolidColorBrush.GetColor","IXpsOMSolidColorBrush::GetColor","xps.ixpsomsolidcolorbrush_getcolor","xpsobjectmodel/IXpsOMSolidColorBrush::GetColor"]
old-location: xps\ixpsomsolidcolorbrush_getcolor.htm
tech.root: xps
ms.assetid: 07201e3d-af2f-4b85-ac03-2911c33f348b
ms.date: 12/05/2018
ms.keywords: GetColor, GetColor method [XPS Documents and Packaging], GetColor method [XPS Documents and Packaging],IXpsOMSolidColorBrush interface, IXpsOMSolidColorBrush interface [XPS Documents and Packaging],GetColor method, IXpsOMSolidColorBrush.GetColor, IXpsOMSolidColorBrush::GetColor, xps.ixpsomsolidcolorbrush_getcolor, xpsobjectmodel/IXpsOMSolidColorBrush::GetColor
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
 - IXpsOMSolidColorBrush::GetColor
 - xpsobjectmodel/IXpsOMSolidColorBrush::GetColor
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
 - IXpsOMSolidColorBrush.GetColor
---

# IXpsOMSolidColorBrush::GetColor


## -description

Gets the color value and color profile of the brush.

## -parameters

### -param color [out]

The color value of the brush.

### -param colorProfile [out, retval]

The color profile of the brush. 

If no color profile has been specified for the brush, a <b>NULL</b> pointer is returned.

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
<i>color</i>, <i>colorProfile</i>, or both are <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresource">IXpsOMColorProfileResource</a>



<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush">IXpsOMSolidColorBrush</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/previous-versions/windows/desktop/dd372939(v=vs.85)">XPS_COLOR</a>