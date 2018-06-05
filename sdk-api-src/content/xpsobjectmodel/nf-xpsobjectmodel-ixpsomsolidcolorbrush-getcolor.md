---
UID: NF:xpsobjectmodel.IXpsOMSolidColorBrush.GetColor
title: IXpsOMSolidColorBrush::GetColor
author: windows-sdk-content
description: Gets the color value and color profile of the brush.
old-location: xps\ixpsomsolidcolorbrush_getcolor.htm
old-project: printdocs
ms.assetid: 07201e3d-af2f-4b85-ac03-2911c33f348b
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: GetColor, GetColor method [XPS Documents and Packaging], GetColor method [XPS Documents and Packaging],IXpsOMSolidColorBrush interface, IXpsOMSolidColorBrush interface [XPS Documents and Packaging],GetColor method, IXpsOMSolidColorBrush.GetColor, IXpsOMSolidColorBrush::GetColor, xps.ixpsomsolidcolorbrush_getcolor, xpsobjectmodel/IXpsOMSolidColorBrush::GetColor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XpsObjectModel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: XPS_INTERLEAVING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMSolidColorBrush.GetColor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
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
<i>color</i>, <i>colorProfile</i>, or both are <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8a344300-c3fc-4225-bfa5-d5d33798a094">IXpsOMColorProfileResource</a>



<a href="https://msdn.microsoft.com/26580a25-09d1-4a9b-85c3-aa8ddcc97867">IXpsOMSolidColorBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/710f3ef1-bbc3-416d-9faf-aa4a716007c2">XPS_COLOR</a>
 

 

