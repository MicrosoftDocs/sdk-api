---
UID: NF:xpsobjectmodel.IXpsOMPartResources.GetRemoteDictionaryResources
title: IXpsOMPartResources::GetRemoteDictionaryResources
author: windows-sdk-content
description: Gets the IXpsOMRemoteDictionaryResourceCollection interface that contains the remote resource dictionaries that are used in the XPS document.
old-location: xps\ixpsompartresources_getremotedictionaryresources.htm
tech.root: printdocs
ms.assetid: cb12fe80-9e94-4797-adf5-a1986512bf57
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetRemoteDictionaryResources, GetRemoteDictionaryResources method [XPS Documents and Packaging], GetRemoteDictionaryResources method [XPS Documents and Packaging],IXpsOMPartResources interface, IXpsOMPartResources interface [XPS Documents and Packaging],GetRemoteDictionaryResources method, IXpsOMPartResources.GetRemoteDictionaryResources, IXpsOMPartResources::GetRemoteDictionaryResources, xps.ixpsompartresources_getremotedictionaryresources, xpsobjectmodel/IXpsOMPartResources::GetRemoteDictionaryResources
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
 - IXpsOMPartResources.GetRemoteDictionaryResources
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXpsOMPartResources::GetRemoteDictionaryResources


## -description


Gets the  <a href="https://msdn.microsoft.com/50c9bd7a-226f-4785-96b4-d0b5e861ae37">IXpsOMRemoteDictionaryResourceCollection</a> interface that contains the remote resource dictionaries  that are used in the XPS document.


## -parameters




### -param dictionaryResources [out, retval]

A pointer to the <a href="https://msdn.microsoft.com/50c9bd7a-226f-4785-96b4-d0b5e861ae37">IXpsOMRemoteDictionaryResourceCollection</a> interface that  contains the remote resource dictionaries that are used in the XPS document.


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
<i>dictionaryResources</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



After loading and parsing the resource into the XPS OM, this method might return an error that applies to another resource. This occurs because all of the relationships are parsed when a resource is loaded.




## -see-also




<a href="https://msdn.microsoft.com/9f706f23-25a0-40ee-93f4-3d7ac98ad6ed">IXpsOMPartResources</a>



<a href="https://msdn.microsoft.com/50c9bd7a-226f-4785-96b4-d0b5e861ae37">IXpsOMRemoteDictionaryResourceCollection</a>



<a href="http://go.microsoft.com/?linkid=8435939">XML Paper Specification</a>



<a href="https://msdn.microsoft.com/9e6db1e3-7151-4538-8607-b7185ebc0110">XPS Document Errors</a>
 

 

