---
UID: NF:xpsobjectmodel.IXpsOMLinearGradientBrush.GetEndPoint
title: IXpsOMLinearGradientBrush::GetEndPoint
author: windows-sdk-content
description: Gets the end point of the gradient.
old-location: xps\ixpsomlineargradientbrush_getendpoint.htm
old-project: printdocs
ms.assetid: c8f34c4b-28f1-4a8f-bf8e-9872debc9eb1
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: GetEndPoint, GetEndPoint method [XPS Documents and Packaging], GetEndPoint method [XPS Documents and Packaging],IXpsOMLinearGradientBrush interface, IXpsOMLinearGradientBrush interface [XPS Documents and Packaging],GetEndPoint method, IXpsOMLinearGradientBrush.GetEndPoint, IXpsOMLinearGradientBrush::GetEndPoint, xps.ixpsomlineargradientbrush_getendpoint, xpsobjectmodel/IXpsOMLinearGradientBrush::GetEndPoint
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
req.typenames: XPS_INTERLEAVING
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xpsobjectmodel.h
api_name:
-	IXpsOMLinearGradientBrush.GetEndPoint
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMLinearGradientBrush::GetEndPoint


## -description


Gets the end point of the gradient.


## -parameters




### -param endPoint [out, retval]

The x and y coordinates of the end point.


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
<i>endPoint</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The coordinates are relative to the page and are expressed in units of the transform that is in effect.




## -see-also




<a href="https://msdn.microsoft.com/739bf088-0f09-47c1-9b49-6c279395f15b">IXpsOMLinearGradientBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>



<a href="https://msdn.microsoft.com/3e5f693a-a0e4-41cf-a2a6-1f61c8e189e3">XPS_POINT</a>
 

 

