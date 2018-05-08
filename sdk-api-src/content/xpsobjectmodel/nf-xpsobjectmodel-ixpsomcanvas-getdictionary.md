---
UID: NF:xpsobjectmodel.IXpsOMCanvas.GetDictionary
title: IXpsOMCanvas::GetDictionary
author: windows-driver-content
description: Gets a pointer to the resolved IXpsOMDictionary interface of the dictionary associated with the canvas.
old-location: xps\ixpsomcanvas_getdictionary.htm
old-project: printdocs
ms.assetid: f32b534e-92bf-4e80-9ac1-b2577e076bed
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: GetDictionary, GetDictionary method [XPS Documents and Packaging], GetDictionary method [XPS Documents and Packaging],IXpsOMCanvas interface, IXpsOMCanvas interface [XPS Documents and Packaging],GetDictionary method, IXpsOMCanvas.GetDictionary, IXpsOMCanvas::GetDictionary, xps.ixpsomcanvas_getdictionary, xpsobjectmodel/IXpsOMCanvas::GetDictionary
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
-	IXpsOMCanvas.GetDictionary
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMCanvas::GetDictionary


## -description


Gets a pointer to the resolved <a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a> interface of the dictionary associated with the canvas.


## -parameters




### -param resourceDictionary [out, retval]

A pointer to the resolved <a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a> interface of the dictionary.

The value that is returned in this parameter depends on which method has been most recently called to set the dictionary.

<table>
<tr>
<th>Most recent method called</th>
<th>Object returned in <i>resourceDictionary</i></th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/f6cd655f-8850-4fce-95af-50edbdd38cb1">SetDictionaryLocal</a>


</td>
<td>
The local dictionary  that is set by <a href="https://msdn.microsoft.com/f6cd655f-8850-4fce-95af-50edbdd38cb1">SetDictionaryLocal</a>.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/8f6a80e9-fa66-45fa-bee9-c80a64a4593f">SetDictionaryResource</a>


</td>
<td>
The shared dictionary in the dictionary resource that is set by <a href="https://msdn.microsoft.com/8f6a80e9-fa66-45fa-bee9-c80a64a4593f">SetDictionaryResource</a>.

</td>
</tr>
<tr>
<td>
Neither <a href="https://msdn.microsoft.com/f6cd655f-8850-4fce-95af-50edbdd38cb1">SetDictionaryLocal</a> nor <a href="https://msdn.microsoft.com/8f6a80e9-fa66-45fa-bee9-c80a64a4593f">SetDictionaryResource</a> has been called yet.

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
<i>resourceDictionary</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



<b>GetDictionary</b> can return the interface pointer of a local or remote dictionary.  <a href="https://msdn.microsoft.com/3570ad03-2b68-4294-b236-86bd372876a2">GetOwner</a> can be called to determine whether the dictionary is local or remote.

After loading and parsing the resource into the XPS OM, this method might return an error that applies to another resource. This occurs because all of the relationships are parsed when a resource is loaded.




## -see-also




<a href="https://msdn.microsoft.com/3cb0e1b3-88a8-4724-a3c5-0df416294e62">IXpsOMCanvas</a>



<a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

