---
UID: NF:xpsobjectmodel.IXpsOMGradientBrush.SetSpreadMethod
title: IXpsOMGradientBrush::SetSpreadMethod method
author: windows-driver-content
description: Sets the XPS_SPREAD_METHOD value, which describes how the area outside of the gradient region is to be rendered.
old-location: xps\ixpsomgradientbrush_setspreadmethod.htm
old-project: printdocs
ms.assetid: 2114ba2e-95df-466e-983f-a56491bf891c
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IXpsOMGradientBrush, IXpsOMGradientBrush interface [XPS Documents and Packaging], SetSpreadMethod method, IXpsOMGradientBrush::SetSpreadMethod, SetSpreadMethod method [XPS Documents and Packaging], SetSpreadMethod method [XPS Documents and Packaging], IXpsOMGradientBrush interface, SetSpreadMethod,IXpsOMGradientBrush.SetSpreadMethod, xps.ixpsomgradientbrush_setspreadmethod, xpsobjectmodel/IXpsOMGradientBrush::SetSpreadMethod
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: XPS_INTERLEAVING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMGradientBrush.SetSpreadMethod
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGradientBrush::SetSpreadMethod method


## -description


Sets the <a href="https://msdn.microsoft.com/9c9cadaf-6f38-4a56-942e-78617017a905">XPS_SPREAD_METHOD</a> value, which describes how the area outside of the gradient region is to be rendered.  The gradient region is defined by the start and end points of the gradient.


## -parameters




### -param spreadMethod [in]

The <a href="https://msdn.microsoft.com/9c9cadaf-6f38-4a56-942e-78617017a905">XPS_SPREAD_METHOD</a> value that describes how the area outside of the gradient region  is to be rendered. The gradient region is defined by the linear-gradient brush or radial-gradient brush that inherits this interface.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>spreadMethod</i> parameter was not a valid <a href="https://msdn.microsoft.com/9c9cadaf-6f38-4a56-942e-78617017a905">XPS_SPREAD_METHOD</a> value.

</td>
</tr>
</table>
 




## -remarks



For more information about different types of spread methods, see <a href="https://msdn.microsoft.com/9c9cadaf-6f38-4a56-942e-78617017a905">XPS_SPREAD_METHOD</a>.




## -see-also




<a href="https://msdn.microsoft.com/d381b813-5368-4ffe-a9a1-0f5027ae9d80">IXpsOMGradientBrush</a>



<a href="https://msdn.microsoft.com/739bf088-0f09-47c1-9b49-6c279395f15b">IXpsOMLinearGradientBrush</a>



<a href="https://msdn.microsoft.com/2f5b7b99-64a0-4156-8963-cfceb0d73503">IXpsOMRadialGradientBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/9c9cadaf-6f38-4a56-942e-78617017a905">XPS_SPREAD_METHOD</a>
 

 

