---
UID: NF:xpsobjectmodel.IXpsOMGradientStop.GetColor
title: IXpsOMGradientStop::GetColor (xpsobjectmodel.h)
author: windows-sdk-content
description: Gets the color value and color profile of the gradient stop.
old-location: xps\ixpsomgradientstop_getcolor.htm
tech.root: printdocs
ms.assetid: 6630d58f-d0f0-4b39-a14c-d3955f0f401a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetColor, GetColor method [XPS Documents and Packaging], GetColor method [XPS Documents and Packaging],IXpsOMGradientStop interface, IXpsOMGradientStop interface [XPS Documents and Packaging],GetColor method, IXpsOMGradientStop.GetColor, IXpsOMGradientStop::GetColor, xps.ixpsomgradientstop_getcolor, xpsobjectmodel/IXpsOMGradientStop::GetColor
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMGradientStop.GetColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMGradientStop::GetColor


## -description


Gets the color value and color profile of the gradient stop.


## -parameters




### -param color [out]

The color value of the gradient stop.


### -param colorProfile [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/8a344300-c3fc-4225-bfa5-d5d33798a094">IXpsOMColorProfileResource</a> interface that contains the color profile to be used. If no color profile resource has been set, a <b>NULL</b> pointer is returned. See remarks.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the table that follows. For information about  XPS document API return values that are not listed in this table, see <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.

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



A color profile is only returned when the color type of <i>color</i> is <a href="https://msdn.microsoft.com/en-us/library/Dd372941(v=VS.85).aspx">XPS_COLOR_TYPE_CONTEXT</a>.




## -see-also




<a href="https://msdn.microsoft.com/8a344300-c3fc-4225-bfa5-d5d33798a094">IXpsOMColorProfileResource</a>



<a href="https://msdn.microsoft.com/e115d806-70c1-4c6a-810e-e6a058628b44">IXpsOMGradientStop</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/710f3ef1-bbc3-416d-9faf-aa4a716007c2">XPS_COLOR</a>
 

 

