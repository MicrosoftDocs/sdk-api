---
UID: NF:xpsobjectmodel.IXpsOMVisual.GetOpacityMaskBrushLocal
title: IXpsOMVisual::GetOpacityMaskBrushLocal
author: windows-sdk-content
description: Gets the local, unshared opacity mask brush for the visual.
old-location: xps\ixpsomvisual_getopacitymaskbrushlocal.htm
old-project: printdocs
ms.assetid: 654dc003-25a6-4186-9c3b-7fe6f82b5481
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: GetOpacityMaskBrushLocal, GetOpacityMaskBrushLocal method [XPS Documents and Packaging], GetOpacityMaskBrushLocal method [XPS Documents and Packaging],IXpsOMVisual interface, IXpsOMVisual interface [XPS Documents and Packaging],GetOpacityMaskBrushLocal method, IXpsOMVisual.GetOpacityMaskBrushLocal, IXpsOMVisual::GetOpacityMaskBrushLocal, xps.ixpsomvisual_getopacitymaskbrushlocal, xpsobjectmodel/IXpsOMVisual::GetOpacityMaskBrushLocal
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
-	IXpsOMVisual.GetOpacityMaskBrushLocal
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMVisual::GetOpacityMaskBrushLocal


## -description


Gets the local, unshared opacity mask brush for the visual.


## -parameters




### -param opacityMaskBrush [out, retval]

A pointer to the  <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a> interface of the visual's opacity mask brush. If an opacity mask brush lookup key has been set, or if a local opacity mask brush has not been set, a <b>NULL</b> pointer is returned.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>opacityMaskBrush</i></th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/d1b84156-b7ad-4dac-97d9-60aaedcee210">SetOpacityMaskBrushLocal</a>


</td>
<td>
The local opacity mask brush that is set by <a href="https://msdn.microsoft.com/d1b84156-b7ad-4dac-97d9-60aaedcee210">SetOpacityMaskBrushLocal</a>.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/93c76649-dc48-4ccf-b1c5-2fb223c93513">SetOpacityMaskBrushLookup</a>


</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>
Neither <a href="https://msdn.microsoft.com/d1b84156-b7ad-4dac-97d9-60aaedcee210">SetOpacityMaskBrushLocal</a> nor <a href="https://msdn.microsoft.com/93c76649-dc48-4ccf-b1c5-2fb223c93513">SetOpacityMaskBrushLookup</a> has been called yet.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
</table>
 


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
<i>opacityMaskBrush</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a>



<a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

