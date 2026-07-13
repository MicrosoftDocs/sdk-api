---
UID: NF:xpsobjectmodel.IXpsOMGradientBrush.GetColorInterpolationMode
title: IXpsOMGradientBrush::GetColorInterpolationMode (xpsobjectmodel.h)
description: Gets the gamma function to be used for color interpolation.
helpviewer_keywords: ["GetColorInterpolationMode","GetColorInterpolationMode method [XPS Documents and Packaging]","GetColorInterpolationMode method [XPS Documents and Packaging]","IXpsOMGradientBrush interface","IXpsOMGradientBrush interface [XPS Documents and Packaging]","GetColorInterpolationMode method","IXpsOMGradientBrush.GetColorInterpolationMode","IXpsOMGradientBrush::GetColorInterpolationMode","xps.ixpsomgradientbrush_getcolorinterpolationmode","xpsobjectmodel/IXpsOMGradientBrush::GetColorInterpolationMode"]
old-location: xps\ixpsomgradientbrush_getcolorinterpolationmode.htm
tech.root: xps
ms.assetid: 4e58c019-d89d-472d-9b6f-b335b184f998
ms.date: 12/05/2018
ms.keywords: GetColorInterpolationMode, GetColorInterpolationMode method [XPS Documents and Packaging], GetColorInterpolationMode method [XPS Documents and Packaging],IXpsOMGradientBrush interface, IXpsOMGradientBrush interface [XPS Documents and Packaging],GetColorInterpolationMode method, IXpsOMGradientBrush.GetColorInterpolationMode, IXpsOMGradientBrush::GetColorInterpolationMode, xps.ixpsomgradientbrush_getcolorinterpolationmode, xpsobjectmodel/IXpsOMGradientBrush::GetColorInterpolationMode
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
 - IXpsOMGradientBrush::GetColorInterpolationMode
 - xpsobjectmodel/IXpsOMGradientBrush::GetColorInterpolationMode
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
 - IXpsOMGradientBrush.GetColorInterpolationMode
---

# IXpsOMGradientBrush::GetColorInterpolationMode


## -description

Gets the gamma function to be used for color interpolation.

## -parameters

### -param colorInterpolationMode [out, retval]

The <a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_color_interpolation">XPS_COLOR_INTERPOLATION</a> value that describes the gamma function to be used for color interpolation.

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
<i>colorInterpolationMode</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush">IXpsOMGradientBrush</a>



<a href="https://en.wikipedia.org/wiki/Open_XML_Paper_Specification">XML Paper Specification</a>



<a href="/previous-versions/windows/desktop/dd372955(v=vs.85)">XPS Document Errors</a>



<a href="/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_color_interpolation">XPS_COLOR_INTERPOLATION</a>