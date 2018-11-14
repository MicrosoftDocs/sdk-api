---
UID: NF:xpsobjectmodel.IXpsOMPath.SetFillBrushLookup
title: IXpsOMPath::SetFillBrushLookup
author: windows-sdk-content
description: Sets the lookup key name of a shared brush in a resource dictionary, to be used as the fill brush.
old-location: xps\ixpsompath_setfillbrushlookup.htm
tech.root: printdocs
ms.assetid: 5a02af98-8bfc-4fb2-92b3-15b16b4b69c1
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IXpsOMPath interface [XPS Documents and Packaging],SetFillBrushLookup method, IXpsOMPath.SetFillBrushLookup, IXpsOMPath::SetFillBrushLookup, SetFillBrushLookup, SetFillBrushLookup method [XPS Documents and Packaging], SetFillBrushLookup method [XPS Documents and Packaging],IXpsOMPath interface, xps.ixpsompath_setfillbrushlookup, xpsobjectmodel/IXpsOMPath::SetFillBrushLookup
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
 - IXpsOMPath.SetFillBrushLookup
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
- IXpsOMPath.SetFillBrushLookup
: 
---

# IXpsOMPath::SetFillBrushLookup


## -description


Sets the lookup key name of a shared brush in a resource dictionary, to be used as the fill brush.


## -parameters




### -param lookup [in]

The key name of the brush in a resource dictionary, to be used as the fill brush.


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



After you call <b>SetFillBrushLookup</b>, the local fill brush is released and <a href="https://msdn.microsoft.com/5c5a7150-19d6-40aa-871b-5600c0b0a947">GetFillBrushLocal</a> returns a <b>NULL</b> pointer in the <i>brush</i> parameter. The table that follows explains the relationship between the local and lookup values of this property.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>brush</i> by <a href="https://msdn.microsoft.com/fc121659-c04f-433a-aaf7-ab7ecd1fd763">GetFillBrush</a>
</th>
<th>Object that is returned in <i>brush</i>  by <a href="https://msdn.microsoft.com/5c5a7150-19d6-40aa-871b-5600c0b0a947">GetFillBrushLocal</a>
</th>
<th>String that is returned in <i>lookup</i> by <a href="https://msdn.microsoft.com/89433357-fa39-41e9-bd21-ff3c076261db">GetFillBrushLookup</a>
</th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/ddec7d68-16a5-4c34-87c1-6a5de97aaa0c">SetFillBrushLocal</a>


</td>
<td>
The local brush that is set by <a href="https://msdn.microsoft.com/ddec7d68-16a5-4c34-87c1-6a5de97aaa0c">SetFillBrushLocal</a>.

</td>
<td>
The local brush that is set by <a href="https://msdn.microsoft.com/ddec7d68-16a5-4c34-87c1-6a5de97aaa0c">SetFillBrushLocal</a>.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>
<b>SetFillBrushLookup</b> (this method)

</td>
<td>
The shared brush retrieved, with a lookup key that matches the key that is set by <b>SetFillBrushLookup</b>, from the resource directory.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The lookup key that is set by <b>SetFillBrushLookup</b>.

</td>
</tr>
<tr>
<td>
Neither <a href="https://msdn.microsoft.com/ddec7d68-16a5-4c34-87c1-6a5de97aaa0c">SetFillBrushLocal</a> nor <b>SetFillBrushLookup</b> has been called yet.

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
 

 

