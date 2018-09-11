---
UID: NF:xpsobjectmodel.IXpsOMCanvas.GetDictionaryLocal
title: IXpsOMCanvas::GetDictionaryLocal
author: windows-sdk-content
description: Gets a pointer to the IXpsOMDictionary interface of the local, unshared dictionary.
old-location: xps\ixpsomcanvas_getdictionarylocal.htm
tech.root: printdocs
ms.assetid: 5578ae0f-4da7-4d9f-9133-fbe501ff66a1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetDictionaryLocal, GetDictionaryLocal method [XPS Documents and Packaging], GetDictionaryLocal method [XPS Documents and Packaging],IXpsOMCanvas interface, IXpsOMCanvas interface [XPS Documents and Packaging],GetDictionaryLocal method, IXpsOMCanvas.GetDictionaryLocal, IXpsOMCanvas::GetDictionaryLocal, xps.ixpsomcanvas_getdictionarylocal, xpsobjectmodel/IXpsOMCanvas::GetDictionaryLocal
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
 - IXpsOMCanvas.GetDictionaryLocal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMCanvas::GetDictionaryLocal


## -description


Gets a pointer to the <a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a> interface of the local, unshared dictionary.


## -parameters




### -param resourceDictionary [out, retval]

The <a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a> interface pointer to the local, unshared dictionary, if one has been set. If a local dictionary has not been set or if a remote dictionary resource has been set, a <b>NULL</b> pointer is returned.

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
The local dictionary that is set by <a href="https://msdn.microsoft.com/f6cd655f-8850-4fce-95af-50edbdd38cb1">SetDictionaryLocal</a>.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/8f6a80e9-fa66-45fa-bee9-c80a64a4593f">SetDictionaryResource</a>


</td>
<td>
<b>NULL</b> pointer.

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



When this method loads and parses the resource into the XPS OM, it might return an error that applies to another resource. This can occur because all of the relationships are parsed when the resource is loaded. 

For more information about other return values that might be returned by this method, see <a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>.




## -see-also




<a href="https://msdn.microsoft.com/3cb0e1b3-88a8-4724-a3c5-0df416294e62">IXpsOMCanvas</a>



<a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

