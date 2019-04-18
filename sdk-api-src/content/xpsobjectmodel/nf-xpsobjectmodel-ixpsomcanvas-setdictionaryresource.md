---
UID: NF:xpsobjectmodel.IXpsOMCanvas.SetDictionaryResource
title: IXpsOMCanvas::SetDictionaryResource (xpsobjectmodel.h)
author: windows-sdk-content
description: Sets the IXpsOMRemoteDictionaryResource interface pointer of the remote dictionary resource.
old-location: xps\ixpsomcanvas_setdictionaryresource.htm
tech.root: printdocs
ms.assetid: 8f6a80e9-fa66-45fa-bee9-c80a64a4593f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IXpsOMCanvas interface [XPS Documents and Packaging],SetDictionaryResource method, IXpsOMCanvas.SetDictionaryResource, IXpsOMCanvas::SetDictionaryResource, SetDictionaryResource, SetDictionaryResource method [XPS Documents and Packaging], SetDictionaryResource method [XPS Documents and Packaging],IXpsOMCanvas interface, xps.ixpsomcanvas_setdictionaryresource, xpsobjectmodel/IXpsOMCanvas::SetDictionaryResource
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
 - IXpsOMCanvas.SetDictionaryResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IXpsOMCanvas::SetDictionaryResource


## -description


Sets the <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface pointer of the remote dictionary resource.


## -parameters




### -param remoteDictionaryResource [in]

The <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface of the remote dictionary resource. A <b>NULL</b> pointer releases any previously assigned dictionary resource.


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
<i>remoteDictionaryResource</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>
 




## -remarks



After calling this method,  <a href="https://msdn.microsoft.com/5578ae0f-4da7-4d9f-9133-fbe501ff66a1">GetDictionaryLocal</a>  returns a <b>NULL</b> pointer in the <i>resourceDictionary</i> parameter.

<table>
<tr>
<th>Most recent method called</th>
<th>Object that is returned in <i>resourceDictionary</i> by <a href="https://msdn.microsoft.com/f32b534e-92bf-4e80-9ac1-b2577e076bed">GetDictionary</a>
</th>
<th>Object that is returned in <i>resourceDictionary</i>     by <a href="https://msdn.microsoft.com/5578ae0f-4da7-4d9f-9133-fbe501ff66a1">GetDictionaryLocal</a>
</th>
<th>Object that is returned in  <i>remoteDictionaryResource</i> by <a href="https://msdn.microsoft.com/96fa8c03-ce00-4d10-8a88-228600fdcae7">GetDictionaryResource</a>
</th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/f6cd655f-8850-4fce-95af-50edbdd38cb1">SetDictionaryLocal</a>


</td>
<td>
The local dictionary that is set by <a href="https://msdn.microsoft.com/f6cd655f-8850-4fce-95af-50edbdd38cb1">SetDictionaryLocal</a>.

</td>
<td>
The local dictionary that is set by <a href="https://msdn.microsoft.com/f6cd655f-8850-4fce-95af-50edbdd38cb1">SetDictionaryLocal</a>.

</td>
<td>
<b>NULL</b> pointer.

</td>
</tr>
<tr>
<td>
<b>SetDictionaryResource</b> (this method)

</td>
<td>
The shared dictionary in the dictionary resource that is set by <b>SetDictionaryResource</b>.

</td>
<td>
<b>NULL</b> pointer.

</td>
<td>
The remote dictionary resource that is set by <b>SetDictionaryResource</b>.

</td>
</tr>
<tr>
<td>
Neither <a href="https://msdn.microsoft.com/f6cd655f-8850-4fce-95af-50edbdd38cb1">SetDictionaryLocal</a> nor <b>SetDictionaryResource</b> has been called yet.

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
 

 

