---
UID: NF:xpsobjectmodel.IXpsOMCanvas.GetDictionaryResource
title: IXpsOMCanvas::GetDictionaryResource
author: windows-sdk-content
description: Gets a pointer to the IXpsOMRemoteDictionaryResource interface of the remote dictionary resource.
old-location: xps\ixpsomcanvas_getdictionaryresource.htm
tech.root: printdocs
ms.assetid: 96fa8c03-ce00-4d10-8a88-228600fdcae7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDictionaryResource, GetDictionaryResource method [XPS Documents and Packaging], GetDictionaryResource method [XPS Documents and Packaging],IXpsOMCanvas interface, IXpsOMCanvas interface [XPS Documents and Packaging],GetDictionaryResource method, IXpsOMCanvas.GetDictionaryResource, IXpsOMCanvas::GetDictionaryResource, xps.ixpsomcanvas_getdictionaryresource, xpsobjectmodel/IXpsOMCanvas::GetDictionaryResource
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
 - IXpsOMCanvas.GetDictionaryResource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMCanvas::GetDictionaryResource


## -description


Gets a pointer to the <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface of the remote dictionary resource.


## -parameters




### -param remoteDictionaryResource [out, retval]

The <a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a> interface pointer to the remote dictionary resource, if one has been set. If a remote dictionary resource has not been set or if a local dictionary resource has been set, a <b>NULL</b> pointer is returned.

<table>
<tr>
<th>Most recent method called</th>
<th>Object returned in <i>remoteDictionaryResource</i></th>
</tr>
<tr>
<td>

<a href="https://msdn.microsoft.com/f6cd655f-8850-4fce-95af-50edbdd38cb1">SetDictionaryLocal</a>


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
The remote dictionary resource that is set by <a href="https://msdn.microsoft.com/8f6a80e9-fa66-45fa-bee9-c80a64a4593f">SetDictionaryResource</a>.

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
<i>remoteDictionaryResource</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



After loading and parsing the resource into the XPS OM, this method might return an error that applies to another resource. This occurs because all of the relationships are parsed when a resource is loaded.




## -see-also




<a href="https://msdn.microsoft.com/3cb0e1b3-88a8-4724-a3c5-0df416294e62">IXpsOMCanvas</a>



<a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

