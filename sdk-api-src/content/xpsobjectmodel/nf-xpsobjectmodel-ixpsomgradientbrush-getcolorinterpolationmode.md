---
UID: NF:xpsobjectmodel.IXpsOMGradientBrush.GetColorInterpolationMode
title: IXpsOMGradientBrush::GetColorInterpolationMode (xpsobjectmodel.h)
author: windows-sdk-content
description: Gets the gamma function to be used for color interpolation.
old-location: xps\ixpsomgradientbrush_getcolorinterpolationmode.htm
tech.root: printdocs
ms.assetid: 4e58c019-d89d-472d-9b6f-b335b184f998
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetColorInterpolationMode, GetColorInterpolationMode method [XPS Documents and Packaging], GetColorInterpolationMode method [XPS Documents and Packaging],IXpsOMGradientBrush interface, IXpsOMGradientBrush interface [XPS Documents and Packaging],GetColorInterpolationMode method, IXpsOMGradientBrush.GetColorInterpolationMode, IXpsOMGradientBrush::GetColorInterpolationMode, xps.ixpsomgradientbrush_getcolorinterpolationmode, xpsobjectmodel/IXpsOMGradientBrush::GetColorInterpolationMode
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
 - IXpsOMGradientBrush.GetColorInterpolationMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMGradientBrush::GetColorInterpolationMode


## -description


Gets the gamma function to be used for color interpolation.


## -parameters




### -param colorInterpolationMode [out, retval]

The <a href="https://msdn.microsoft.com/en-us/library/Dd372940(v=VS.85).aspx">XPS_COLOR_INTERPOLATION</a> value that describes the gamma function to be used for color interpolation.


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
<i>colorInterpolationMode</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d381b813-5368-4ffe-a9a1-0f5027ae9d80">IXpsOMGradientBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd372940(v=VS.85).aspx">XPS_COLOR_INTERPOLATION</a>
 

 

