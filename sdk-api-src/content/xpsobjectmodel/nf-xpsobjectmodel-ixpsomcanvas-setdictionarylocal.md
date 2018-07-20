---
UID: NF:xpsobjectmodel.IXpsOMCanvas.SetDictionaryLocal
title: IXpsOMCanvas::SetDictionaryLocal
author: windows-sdk-content
description: Sets the IXpsOMDictionary interface pointer of the local, unshared dictionary.
old-location: xps\ixpsomcanvas_setdictionarylocal.htm
old-project: printdocs
ms.assetid: f6cd655f-8850-4fce-95af-50edbdd38cb1
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IXpsOMCanvas interface [XPS Documents and Packaging],SetDictionaryLocal method, IXpsOMCanvas.SetDictionaryLocal, IXpsOMCanvas::SetDictionaryLocal, SetDictionaryLocal, SetDictionaryLocal method [XPS Documents and Packaging], SetDictionaryLocal method [XPS Documents and Packaging],IXpsOMCanvas interface, xps.ixpsomcanvas_setdictionarylocal, xpsobjectmodel/IXpsOMCanvas::SetDictionaryLocal
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
 - IXpsOMCanvas.SetDictionaryLocal
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXpsOMCanvas::SetDictionaryLocal


## -description


Sets the <a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a> interface pointer of the local, unshared dictionary.


## -parameters




### -param resourceDictionary [in]

The <a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a> interface of the local, unshared dictionary. A <b>NULL</b> pointer releases  any previously assigned local dictionary.


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
<i>resourceDictionary</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>
 




## -remarks



After you call <b>SetDictionaryLocal</b>, the remote dictionary resource is released and <a href="https://msdn.microsoft.com/96fa8c03-ce00-4d10-8a88-228600fdcae7">GetDictionaryResource</a> returns a <b>NULL</b> pointer in the <i>remoteDictionaryResource</i> parameter. The table that follows explains the relationship between the local and remote values of this property.


<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned  in  <i>resourceDictionary</i>  by <a href="https://msdn.microsoft.com/f32b534e-92bf-4e80-9ac1-b2577e076bed">GetDictionary</a>
</th>
<th>Object that is returned in <i>resourceDictionary</i>  by <a href="https://msdn.microsoft.com/5578ae0f-4da7-4d9f-9133-fbe501ff66a1">GetDictionaryLocal</a>
</th>
<th>Object that is returned in <i>remoteDictionaryResource</i>  by <a href="https://msdn.microsoft.com/96fa8c03-ce00-4d10-8a88-228600fdcae7">GetDictionaryResource</a>
</th>
</tr>
<tr>
<td>
<b>SetDictionaryLocal</b> (this method)

</td>
<td>
The local dictionary that is set by <b>SetDictionaryLocal</b>.

</td>
<td>
The local dictionary that is set by <b>SetDictionaryLocal</b>.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/8f6a80e9-fa66-45fa-bee9-c80a64a4593f">SetDictionaryResource</a>


</td>
<td>
The shared dictionary in the dictionary resource that is set by <a href="https://msdn.microsoft.com/8f6a80e9-fa66-45fa-bee9-c80a64a4593f">SetDictionaryResource</a>.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The remote dictionary resource that is set by <a href="https://msdn.microsoft.com/8f6a80e9-fa66-45fa-bee9-c80a64a4593f">SetDictionaryResource</a>.

</td>
</tr>
<tr>
<td>
Neither <b>SetDictionaryLocal</b> nor <a href="https://msdn.microsoft.com/8f6a80e9-fa66-45fa-bee9-c80a64a4593f">SetDictionaryResource</a> has been called yet.

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




<a href="https://msdn.microsoft.com/3cb0e1b3-88a8-4724-a3c5-0df416294e62">IXpsOMCanvas</a>



<a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

