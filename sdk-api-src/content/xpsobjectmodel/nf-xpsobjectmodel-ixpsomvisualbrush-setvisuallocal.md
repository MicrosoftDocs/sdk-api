---
UID: NF:xpsobjectmodel.IXpsOMVisualBrush.SetVisualLocal
title: IXpsOMVisualBrush::SetVisualLocal
author: windows-sdk-content
description: Sets the interface pointer of the local, unshared visual used as the source for the brush.
old-location: xps\ixpsomvisualbrush_setvisuallocal.htm
tech.root: printdocs
ms.assetid: 8ef37838-ff5f-4c8f-9fa3-30d11417c09d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IXpsOMVisualBrush interface [XPS Documents and Packaging],SetVisualLocal method, IXpsOMVisualBrush.SetVisualLocal, IXpsOMVisualBrush::SetVisualLocal, SetVisualLocal, SetVisualLocal method [XPS Documents and Packaging], SetVisualLocal method [XPS Documents and Packaging],IXpsOMVisualBrush interface, xps.ixpsomvisualbrush_setvisuallocal, xpsobjectmodel/IXpsOMVisualBrush::SetVisualLocal
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
 - IXpsOMVisualBrush.SetVisualLocal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMVisualBrush::SetVisualLocal


## -description


Sets the interface pointer of the local, unshared visual used as the source for the brush.


## -parameters




### -param visual [in]

A pointer to the <a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a> interface to be set as the visual for the brush. If a local visual has been set, passing a  <b>NULL</b> pointer will release it.


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
<i>visual</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>
 




## -remarks



After you call <b>SetVisualLocal</b>, the visual lookup key is released and <a href="https://msdn.microsoft.com/091cb7f3-6302-40a0-b509-c72e20109f75">GetVisualLookup</a> returns a <b>NULL</b> pointer in the <i>lookup</i> parameter. The table that follows explains the relationship between the local and lookup values of this property.


<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned  in <i>visual</i> by <a href="https://msdn.microsoft.com/b8fb6698-8ce7-42a1-bad6-bde3d5dbbbf8">GetVisual</a>
</th>
<th>Object that is returned  in <i>visual</i> by <a href="https://msdn.microsoft.com/a75c2bca-eaac-4382-9211-fbc1b05f1414">GetVisualLocal</a>
</th>
<th>String that is returned  in <i>lookup</i> by <a href="https://msdn.microsoft.com/091cb7f3-6302-40a0-b509-c72e20109f75">GetVisualLookup</a>
</th>
</tr>
<tr>
<td>
<b>SetVisualLocal</b> (this method).

</td>
<td>
The visual  that is set by <b>SetVisualLocal</b>.

</td>
<td>
The visual  that is set by <b>SetVisualLocal</b>.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/ab98d93c-76fe-477b-9032-c54c0e22a176">SetVisualLookup</a>


</td>
<td>
The visual that is retrieved, with a lookup key that matches the key that is set by <a href="https://msdn.microsoft.com/ab98d93c-76fe-477b-9032-c54c0e22a176">SetVisualLookup</a>, from the resource directory.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The lookup key that is set by <a href="https://msdn.microsoft.com/ab98d93c-76fe-477b-9032-c54c0e22a176">SetVisualLookup</a>.

</td>
</tr>
<tr>
<td>
Neither <b>SetVisualLocal</b> nor <a href="https://msdn.microsoft.com/ab98d93c-76fe-477b-9032-c54c0e22a176">SetVisualLookup</a> has been called yet.

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




<a href="https://msdn.microsoft.com/f2ec412c-aece-4b20-a721-e6c17615e56b">IXpsOMVisual</a>



<a href="https://msdn.microsoft.com/56c11e64-64a8-4c42-9547-4f1fcdc13a4b">IXpsOMVisualBrush</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

