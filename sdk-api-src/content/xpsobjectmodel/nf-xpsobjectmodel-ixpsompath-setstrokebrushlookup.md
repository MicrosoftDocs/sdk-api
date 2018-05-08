---
UID: NF:xpsobjectmodel.IXpsOMPath.SetStrokeBrushLookup
title: IXpsOMPath::SetStrokeBrushLookup
author: windows-driver-content
description: Sets the lookup key name of a shared brush to be used as the stroke brush.
old-location: xps\ixpsompath_setstrokebrushlookup.htm
old-project: printdocs
ms.assetid: b2af731a-bea7-4f1b-8e31-b0173e38fd67
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IXpsOMPath interface [XPS Documents and Packaging],SetStrokeBrushLookup method, IXpsOMPath.SetStrokeBrushLookup, IXpsOMPath::SetStrokeBrushLookup, SetStrokeBrushLookup, SetStrokeBrushLookup method [XPS Documents and Packaging], SetStrokeBrushLookup method [XPS Documents and Packaging],IXpsOMPath interface, xps.ixpsompath_setstrokebrushlookup, xpsobjectmodel/IXpsOMPath::SetStrokeBrushLookup
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
-	IXpsOMPath.SetStrokeBrushLookup
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPath::SetStrokeBrushLookup


## -description


Sets the lookup key name of a shared brush to be used as the stroke brush.

  The shared brush is stored in a resource dictionary.


## -parameters




### -param lookup [in]

The lookup key name of a shared brush to be used as the  stroke brush for the path.


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
<dt><b>XPS_E_INVALID_RESOURCE_KEY</b></dt>
</dl>
</td>
<td width="60%">
According to the <a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>, the value of <i>lookup</i> is not a valid lookup key string.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_INVALID_LOOKUP_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The lookup key name in <i>lookup</i> references an object that is not a brush.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XPS_E_LOOKUP_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
No object could be found with a key name that matched the value passed in <i>lookup</i>.

</td>
</tr>
</table>
 




## -remarks



After you call <b>SetStrokeBrushLookup</b>, the local stroke brush is released and <a href="https://msdn.microsoft.com/cf816750-8381-4c04-af20-e5ce3f8ad63c">GetStrokeBrushLocal</a> returns a <b>NULL</b> pointer in the <i>brush</i> parameter. The table that follows explains the relationship between the local and lookup values of this property.

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

<a href="https://msdn.microsoft.com/551bc4e2-2bf3-455b-a7f1-35b3b66697c0">SetStrokeBrushLocal</a>


</td>
<td>
The local brush that is set by <a href="https://msdn.microsoft.com/551bc4e2-2bf3-455b-a7f1-35b3b66697c0">SetStrokeBrushLocal</a>.

</td>
<td>
The local brush that is set by <a href="https://msdn.microsoft.com/551bc4e2-2bf3-455b-a7f1-35b3b66697c0">SetStrokeBrushLocal</a>.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>
<b>SetStrokeBrushLookup</b>(this method)

</td>
<td>
The shared brush retrieved, with a lookup key that matches the key that is set by <b>SetStrokeBrushLookup</b>, from the resource directory.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The lookup key that is set by <b>SetStrokeBrushLookup</b>.

</td>
</tr>
<tr>
<td>
Neither <a href="https://msdn.microsoft.com/551bc4e2-2bf3-455b-a7f1-35b3b66697c0">SetStrokeBrushLocal</a> nor <b>SetStrokeBrushLookup</b> has been called yet.

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




<a href="https://msdn.microsoft.com/93257a77-3fef-400e-bfe1-06e760ba4b93">IXpsOMPath</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

