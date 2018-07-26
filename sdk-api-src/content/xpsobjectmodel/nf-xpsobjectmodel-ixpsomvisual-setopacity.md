---
UID: NF:xpsobjectmodel.IXpsOMVisual.SetOpacity
title: IXpsOMVisual::SetOpacity
author: windows-sdk-content
description: Sets the opacity value of the visual.
old-location: xps\ixpsomvisual_setopacity.htm
old-project: printdocs
ms.assetid: 2a29aee3-f11b-41e7-a871-3be3d5994409
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IXpsOMVisual interface [XPS Documents and Packaging],SetOpacity method, IXpsOMVisual.SetOpacity, IXpsOMVisual::SetOpacity, SetOpacity, SetOpacity method [XPS Documents and Packaging], SetOpacity method [XPS Documents and Packaging],IXpsOMVisual interface, xps.ixpsomvisual_setopacity, xpsobjectmodel/IXpsOMVisual::SetOpacity
ms.prod: windows
ms.technology: windows-sdk
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
 - IXpsOMVisual.SetOpacity
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMVisual::SetOpacity


## -description


Sets the opacity value of the visual.


## -parameters




### -param opacity [in]

The opacity value to be set for the visual. 

The range of allowed values for this parameter is 0.0  to 1.0; with 0.0 the visual is completely transparent, and with 1.0 it is completely opaque.


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
<i>opacity</i> contains a value that is not allowed.
              

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

