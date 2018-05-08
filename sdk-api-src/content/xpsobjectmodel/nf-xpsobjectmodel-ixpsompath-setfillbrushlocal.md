---
UID: NF:xpsobjectmodel.IXpsOMPath.SetFillBrushLocal
title: IXpsOMPath::SetFillBrushLocal
author: windows-driver-content
description: Sets the pointer to the local, unshared IXpsOMBrush interface to be used as the fill brush.
old-location: xps\ixpsompath_setfillbrushlocal.htm
old-project: printdocs
ms.assetid: ddec7d68-16a5-4c34-87c1-6a5de97aaa0c
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IXpsOMPath interface [XPS Documents and Packaging],SetFillBrushLocal method, IXpsOMPath.SetFillBrushLocal, IXpsOMPath::SetFillBrushLocal, SetFillBrushLocal, SetFillBrushLocal method [XPS Documents and Packaging], SetFillBrushLocal method [XPS Documents and Packaging],IXpsOMPath interface, xps.ixpsompath_setfillbrushlocal, xpsobjectmodel/IXpsOMPath::SetFillBrushLocal
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
-	IXpsOMPath.SetFillBrushLocal
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMPath::SetFillBrushLocal


## -description


Sets the pointer to the local, unshared <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a> interface to be used as the fill brush.


## -parameters




### -param brush [in]

A pointer to the local, unshared <a href="https://msdn.microsoft.com/43cb56db-e09e-47cb-b50b-7827131659fd">IXpsOMBrush</a> interface to be used as the fill brush.


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



After you call <b>SetFillBrushLocal</b>, the fill brush lookup key is released and <a href="https://msdn.microsoft.com/89433357-fa39-41e9-bd21-ff3c076261db">GetFillBrushLookup</a> returns a <b>NULL</b> pointer in the <i>lookup</i> parameter. The table that follows explains the relationship between the local and lookup values of this property.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>brush</i> by <a href="https://msdn.microsoft.com/fc121659-c04f-433a-aaf7-ab7ecd1fd763">GetFillBrush</a>
</th>
<th>Object that is returned in <i>brush</i> by <a href="https://msdn.microsoft.com/5c5a7150-19d6-40aa-871b-5600c0b0a947">GetFillBrushLocal</a>
</th>
<th>String that is returned in <i>lookup</i> by <a href="https://msdn.microsoft.com/89433357-fa39-41e9-bd21-ff3c076261db">GetFillBrushLookup</a>
</th>
</tr>
<tr>
<td>
<b>SetFillBrushLocal</b> (this method)

</td>
<td>
The local brush that is set by <b>SetFillBrushLocal</b>.

</td>
<td>
The local brush that is set by <b>SetFillBrushLocal</b>.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/5a02af98-8bfc-4fb2-92b3-15b16b4b69c1">SetFillBrushLookup</a>


</td>
<td>
The shared brush retrieved, with a lookup key that matches the key that is set by <a href="https://msdn.microsoft.com/5a02af98-8bfc-4fb2-92b3-15b16b4b69c1">SetFillBrushLookup</a>, from the resource directory.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The lookup key that is set by <a href="https://msdn.microsoft.com/5a02af98-8bfc-4fb2-92b3-15b16b4b69c1">SetFillBrushLookup</a>.

</td>
</tr>
<tr>
<td>
Neither <b>SetFillBrushLocal</b> nor <a href="https://msdn.microsoft.com/5a02af98-8bfc-4fb2-92b3-15b16b4b69c1">SetFillBrushLookup</a> has been called yet.

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
 

 

