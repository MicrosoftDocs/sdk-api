---
UID: NF:xpsobjectmodel.IXpsOMVisual.SetOpacityMaskBrushLocal
title: IXpsOMVisual::SetOpacityMaskBrushLocal
author: windows-sdk-content
description: Sets the IXpsOMBrush interface pointer as the local, unshared opacity mask brush.
old-location: xps\ixpsomvisual_setopacitymaskbrushlocal.htm
tech.root: printdocs
ms.assetid: d1b84156-b7ad-4dac-97d9-60aaedcee210
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IXpsOMVisual interface [XPS Documents and Packaging],SetOpacityMaskBrushLocal method, IXpsOMVisual.SetOpacityMaskBrushLocal, IXpsOMVisual::SetOpacityMaskBrushLocal, SetOpacityMaskBrushLocal, SetOpacityMaskBrushLocal method [XPS Documents and Packaging], SetOpacityMaskBrushLocal method [XPS Documents and Packaging],IXpsOMVisual interface, xps.ixpsomvisual_setopacitymaskbrushlocal, xpsobjectmodel/IXpsOMVisual::SetOpacityMaskBrushLocal
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
 - IXpsOMVisual.SetOpacityMaskBrushLocal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xpsobjectmodel.h
: 
- IXpsOMVisual.SetOpacityMaskBrushLocal
: 
---

# IXpsOMVisual::SetOpacityMaskBrushLocal


## -description


Sets the <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a> interface pointer as the local, unshared opacity mask brush.


## -parameters




### -param opacityMaskBrush [in]

A pointer to the <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a> interface to be set as the local, unshared opacity mask brush. A <b>NULL</b> pointer clears the previously assigned opacity mask brush.


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
<dt><b>XPS_E_NO_CUSTOM_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
<i>opacityMaskBrush</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>
 




## -remarks



After you call <b>SetOpacityMaskBrushLocal</b>, the opacity mask brush lookup key is released and <a href="https://msdn.microsoft.com/84d4aae9-e3e3-4c82-8877-b8206d3678f0">GetOpacityMaskBrushLookup</a> returns a <b>NULL</b> pointer in the <i>key</i> parameter. The table that follows explains the relationship between the local and lookup values of this property.


<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>opacityMaskBrush</i> by <a href="https://msdn.microsoft.com/df5b770e-cc66-45ee-b865-2959255920bf">GetOpacityMaskBrush</a>
</th>
<th>Object that is returned in <i>opacityMaskBrush</i> by <a href="https://msdn.microsoft.com/654dc003-25a6-4186-9c3b-7fe6f82b5481">GetOpacityMaskBrushLocal</a>
</th>
<th>String that is returned in <i>key</i> by <a href="https://msdn.microsoft.com/84d4aae9-e3e3-4c82-8877-b8206d3678f0">GetOpacityMaskBrushLookup</a>
</th>
</tr>
<tr>
<td>
<b>SetOpacityMaskBrushLocal</b> (this method)

</td>
<td>
The local opacity mask brush that is set by <b>SetOpacityMaskBrushLocal</b>.

</td>
<td>
The local opacity mask brush that is set by <b>SetOpacityMaskBrushLocal</b>.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/93c76649-dc48-4ccf-b1c5-2fb223c93513">SetOpacityMaskBrushLookup</a>


</td>
<td>
The shared opacity mask brush that gets retrieved, with a lookup key that matches the key that is set by <a href="https://msdn.microsoft.com/93c76649-dc48-4ccf-b1c5-2fb223c93513">SetOpacityMaskBrushLookup</a>, from the resource directory.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The lookup key that is set by <a href="https://msdn.microsoft.com/93c76649-dc48-4ccf-b1c5-2fb223c93513">SetOpacityMaskBrushLookup</a>.

</td>
</tr>
<tr>
<td>
Neither <b>SetOpacityMaskBrushLocal</b> nor <a href="https://msdn.microsoft.com/93c76649-dc48-4ccf-b1c5-2fb223c93513">SetOpacityMaskBrushLookup</a> has been called yet.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a>



<a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

