---
UID: NF:xpsobjectmodel.IXpsOMGradientBrush.GetSpreadMethod
title: IXpsOMGradientBrush::GetSpreadMethod (xpsobjectmodel.h)
author: windows-sdk-content
description: Gets the XPS_SPREAD_METHOD value, which describes how the area outside of the gradient region will be rendered.
old-location: xps\ixpsomgradientbrush_getspreadmethod.htm
tech.root: printdocs
ms.assetid: c4c62817-735b-4ef1-84cf-1c9fa63f55ee
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSpreadMethod, GetSpreadMethod method [XPS Documents and Packaging], GetSpreadMethod method [XPS Documents and Packaging],IXpsOMGradientBrush interface, IXpsOMGradientBrush interface [XPS Documents and Packaging],GetSpreadMethod method, IXpsOMGradientBrush.GetSpreadMethod, IXpsOMGradientBrush::GetSpreadMethod, xps.ixpsomgradientbrush_getspreadmethod, xpsobjectmodel/IXpsOMGradientBrush::GetSpreadMethod
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
 - IXpsOMGradientBrush.GetSpreadMethod
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMGradientBrush::GetSpreadMethod


## -description


Gets the <a href="https://msdn.microsoft.com/en-us/library/Dd372989(v=VS.85).aspx">XPS_SPREAD_METHOD</a> value, which describes how the area outside of the gradient region will be rendered.


## -parameters




### -param spreadMethod [out, retval]

The <a href="https://msdn.microsoft.com/en-us/library/Dd372989(v=VS.85).aspx">XPS_SPREAD_METHOD</a> value that describes how the area outside of the gradient region will be rendered. The gradient region is defined by the linear-gradient brush or radial-gradient brush that inherits this interface.


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
<i>spreadMethod</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



For more information about different types of spread methods, see <a href="https://msdn.microsoft.com/en-us/library/Dd372989(v=VS.85).aspx">XPS_SPREAD_METHOD</a>.




## -see-also




<a href="https://msdn.microsoft.com/d381b813-5368-4ffe-a9a1-0f5027ae9d80">IXpsOMGradientBrush</a>



<a href="https://msdn.microsoft.com/739bf088-0f09-47c1-9b49-6c279395f15b">IXpsOMLinearGradientBrush</a>



<a href="https://msdn.microsoft.com/2f5b7b99-64a0-4156-8963-cfceb0d73503">IXpsOMRadialGradientBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd372989(v=VS.85).aspx">XPS_SPREAD_METHOD</a>
 

 

