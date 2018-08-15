---
UID: NF:xpsobjectmodel.IXpsOMGradientStop.GetOwner
title: IXpsOMGradientStop::GetOwner
author: windows-sdk-content
description: Gets a pointer to the IXpsOMGradientBrush interface that contains the gradient stop.
old-location: xps\ixpsomgradientstop_getowner.htm
old-project: printdocs
ms.assetid: a590e461-bf86-4379-b29a-ecdba57bd3f8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetOwner, GetOwner method [XPS Documents and Packaging], GetOwner method [XPS Documents and Packaging],IXpsOMGradientStop interface, IXpsOMGradientStop interface [XPS Documents and Packaging],GetOwner method, IXpsOMGradientStop.GetOwner, IXpsOMGradientStop::GetOwner, xps.ixpsomgradientstop_getowner, xpsobjectmodel/IXpsOMGradientStop::GetOwner
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: xpsobjectmodel.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: XPS_INTERLEAVING
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xpsobjectmodel.h
api_name:
 - IXpsOMGradientStop.GetOwner
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMGradientStop::GetOwner


## -description


Gets a pointer to the <a href="https://msdn.microsoft.com/d381b813-5368-4ffe-a9a1-0f5027ae9d80">IXpsOMGradientBrush</a> interface that contains the gradient stop.


## -parameters




### -param owner [out, retval]

A pointer to the  <a href="https://msdn.microsoft.com/d381b813-5368-4ffe-a9a1-0f5027ae9d80">IXpsOMGradientBrush</a> interface that contains the gradient stop. If the gradient stop is not assigned to a gradient brush, a <b>NULL</b> pointer is returned.


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
<i>owner</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d381b813-5368-4ffe-a9a1-0f5027ae9d80">IXpsOMGradientBrush</a>



<a href="https://msdn.microsoft.com/e115d806-70c1-4c6a-810e-e6a058628b44">IXpsOMGradientStop</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

