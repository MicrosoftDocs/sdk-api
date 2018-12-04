---
UID: NF:xpsobjectmodel.IXpsOMSolidColorBrush.SetColor
title: IXpsOMSolidColorBrush::SetColor
author: windows-sdk-content
description: Sets the color value and color profile of the brush.
old-location: xps\ixpsomsolidcolorbrush_setcolor.htm
tech.root: printdocs
ms.assetid: f82fb087-c511-48b7-9e0b-9ec690a86ac7
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IXpsOMSolidColorBrush interface [XPS Documents and Packaging],SetColor method, IXpsOMSolidColorBrush.SetColor, IXpsOMSolidColorBrush::SetColor, SetColor, SetColor method [XPS Documents and Packaging], SetColor method [XPS Documents and Packaging],IXpsOMSolidColorBrush interface, xps.ixpsomsolidcolorbrush_setcolor, xpsobjectmodel/IXpsOMSolidColorBrush::SetColor
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IXpsOMSolidColorBrush.SetColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMSolidColorBrush::SetColor


## -description


Sets the color value and color profile of the brush.


## -parameters




### -param color [in]

The color value of the brush. 

If the value of the <b>colorType</b> field in the <a href="https://msdn.microsoft.com/710f3ef1-bbc3-416d-9faf-aa4a716007c2">XPS_COLOR</a> structure that is passed in this parameter is <a href="https://msdn.microsoft.com/995576a6-ccca-4c0d-8346-2155801a2fbc">XPS_COLOR_TYPE_CONTEXT</a>, a valid color profile must be provided in the <i>colorProfile</i> parameter.


### -param colorProfile [in]

The color profile to be used with <i>color</i>.

A color profile is required when the value of the <b>colorType</b> field in the <a href="https://msdn.microsoft.com/710f3ef1-bbc3-416d-9faf-aa4a716007c2">XPS_COLOR</a> structure that is passed  in the <i>color</i> parameter is <a href="https://msdn.microsoft.com/995576a6-ccca-4c0d-8346-2155801a2fbc">XPS_COLOR_TYPE_CONTEXT</a>. If the value of the <b>colorType</b> field is not <b>XPS_COLOR_TYPE_CONTEXT</b>, this parameter must be set to <b>NULL</b>.


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
<i>colorProfile</i> is <b>NULL</b> when a color profile is expected. A color profile is required when the color type is <a href="https://msdn.microsoft.com/995576a6-ccca-4c0d-8346-2155801a2fbc">XPS_COLOR_TYPE_CONTEXT</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_UNEXPECTED_COLORPROFILE</b></dt>
</dl>
</td>
<td width="60%">
<i>colorProfile</i> has a color profile when none is expected. A color profile is only allowed when the color type is <a href="https://msdn.microsoft.com/995576a6-ccca-4c0d-8346-2155801a2fbc">XPS_COLOR_TYPE_CONTEXT</a>.

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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8a344300-c3fc-4225-bfa5-d5d33798a094">IXpsOMColorProfileResource</a>



<a href="https://msdn.microsoft.com/26580a25-09d1-4a9b-85c3-aa8ddcc97867">IXpsOMSolidColorBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/710f3ef1-bbc3-416d-9faf-aa4a716007c2">XPS_COLOR</a>
 

 

