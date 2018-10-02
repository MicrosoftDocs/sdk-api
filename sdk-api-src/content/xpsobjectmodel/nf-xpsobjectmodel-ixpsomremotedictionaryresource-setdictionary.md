---
UID: NF:xpsobjectmodel.IXpsOMRemoteDictionaryResource.SetDictionary
title: IXpsOMRemoteDictionaryResource::SetDictionary
author: windows-sdk-content
description: Sets a pointer to the IXpsOMDictionary interface of the remote dictionary that is to be associated with this resource.
old-location: xps\ixpsomremotedictionaryresource_setdictionary.htm
tech.root: printdocs
ms.assetid: 68aba55b-d755-4ed3-8ede-6f3a4e6f7b3a
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IXpsOMRemoteDictionaryResource interface [XPS Documents and Packaging],SetDictionary method, IXpsOMRemoteDictionaryResource.SetDictionary, IXpsOMRemoteDictionaryResource::SetDictionary, SetDictionary, SetDictionary method [XPS Documents and Packaging], SetDictionary method [XPS Documents and Packaging],IXpsOMRemoteDictionaryResource interface, xps.ixpsomremotedictionaryresource_setdictionary, xpsobjectmodel/IXpsOMRemoteDictionaryResource::SetDictionary
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
 - IXpsOMRemoteDictionaryResource.SetDictionary
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMRemoteDictionaryResource::SetDictionary


## -description


Sets a   pointer to the <a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a> interface of the remote dictionary that is to be associated with this resource.


## -parameters




### -param dictionary [in]

The <a href="https://msdn.microsoft.com/f887e3d3-973c-4267-a785-6bc190c13082">IXpsOMDictionary</a> interface of the dictionary that is to be associated with this resource.


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
<i>dictionary</i> does not point to a recognized interface implementation. Custom implementation of XPS Document API interfaces is not supported.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/dd757856-f16e-46ad-b865-8203c3428372">IXpsOMRemoteDictionaryResource</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

