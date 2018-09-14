---
UID: NF:xpsobjectmodel.IXpsOMPath.SetStrokeBrushLocal
title: IXpsOMPath::SetStrokeBrushLocal
author: windows-sdk-content
description: Sets a pointer to a local, unshared IXpsOMBrush interface to be used as a stroke brush.
old-location: xps\ixpsompath_setstrokebrushlocal.htm
tech.root: printdocs
ms.assetid: 551bc4e2-2bf3-455b-a7f1-35b3b66697c0
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IXpsOMPath interface [XPS Documents and Packaging],SetStrokeBrushLocal method, IXpsOMPath.SetStrokeBrushLocal, IXpsOMPath::SetStrokeBrushLocal, SetStrokeBrushLocal, SetStrokeBrushLocal method [XPS Documents and Packaging], SetStrokeBrushLocal method [XPS Documents and Packaging],IXpsOMPath interface, xps.ixpsompath_setstrokebrushlocal, xpsobjectmodel/IXpsOMPath::SetStrokeBrushLocal
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
 - IXpsOMPath.SetStrokeBrushLocal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPath::SetStrokeBrushLocal


## -description


Sets a pointer to a local, unshared <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a> interface to be used as a stroke brush.


## -parameters




### -param brush [in]

A pointer to a local, unshared <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a> interface to be used as a stroke brush.


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
<i>brush</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>
 




## -remarks



After you call <b>SetStrokeBrushLocal</b>, the stroke brush lookup key is released and <a href="https://msdn.microsoft.com/af70b6a3-203a-4189-b44d-763539e0302a">GetStrokeBrushLookup</a> returns a <b>NULL</b> pointer in the <i>lookup</i> parameter. The table that follows explains the relationship between the local and lookup values of this property.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>brush</i> by <a href="https://msdn.microsoft.com/dbf786b0-5603-4735-8770-4c5e17a67253">GetStrokeBrush</a>
</th>
<th>Object that is returned in <i>brush</i> by <a href="https://msdn.microsoft.com/cf816750-8381-4c04-af20-e5ce3f8ad63c">GetStrokeBrushLocal</a>
</th>
<th>String that is returned in <i>lookup</i> by <a href="https://msdn.microsoft.com/af70b6a3-203a-4189-b44d-763539e0302a">GetStrokeBrushLookup</a>
</th>
</tr>
<tr>
<td>
<b>SetStrokeBrushLocal</b>  (this method)

</td>
<td>
The local brush that is set by <b>SetStrokeBrushLocal</b>.

</td>
<td>
The local brush that is set by <b>SetStrokeBrushLocal</b>.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/b2af731a-bea7-4f1b-8e31-b0173e38fd67">SetStrokeBrushLookup</a>


</td>
<td>
The shared brush retrieved, with a lookup key that matches the key set by <a href="https://msdn.microsoft.com/b2af731a-bea7-4f1b-8e31-b0173e38fd67">SetStrokeBrushLookup</a>, from the resource directory.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The lookup key that is set by <a href="https://msdn.microsoft.com/b2af731a-bea7-4f1b-8e31-b0173e38fd67">SetStrokeBrushLookup</a>.

</td>
</tr>
<tr>
<td>
Neither <b>SetStrokeBrushLocal</b> nor <a href="https://msdn.microsoft.com/b2af731a-bea7-4f1b-8e31-b0173e38fd67">SetStrokeBrushLookup</a> has been called yet.

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



<a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

