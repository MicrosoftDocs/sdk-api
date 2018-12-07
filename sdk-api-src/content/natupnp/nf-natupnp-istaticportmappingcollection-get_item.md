---
UID: NF:natupnp.IStaticPortMappingCollection.get_Item
title: IStaticPortMappingCollection::get_Item
author: windows-sdk-content
description: The get_Item method retrieves the specified port mapping from the collection.
old-location: ics\istaticportmappingcollection_get_item.htm
tech.root: ics
ms.assetid: 0034e56d-45a1-404a-b129-6ebb951e7d76
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IStaticPortMappingCollection interface [ICS/ICF],get_Item method, IStaticPortMappingCollection.get_Item, IStaticPortMappingCollection::get_Item, _ics_istaticportmappingcollection_get_item, get_Item, get_Item method [ICS/ICF], get_Item method [ICS/ICF],IStaticPortMappingCollection interface, ics.istaticportmappingcollection_get_item, natupnp/IStaticPortMappingCollection::get_Item
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: natupnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Hnetcfg.dll
api_name:
 - IStaticPortMappingCollection.get_Item
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStaticPortMappingCollection::get_Item


## -description


The 
<b>get_Item</b> method retrieves the specified port mapping from the collection.


## -parameters




### -param lExternalPort [in]

Specifies the external port for this port mapping.


### -param bstrProtocol [in]

Specifies the protocol. This parameter should be either UDP or TCP.


### -param ppSPM [out]

Pointer to an interface pointer that points to an 
<a href="https://msdn.microsoft.com/5013fea2-e767-4600-a10c-6859b7be42e4">IStaticPortMapping</a> interface for this port mapping.


## -returns



If the method succeeds the return value is S_OK.

If the method fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
The operation was aborted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
A specified interface is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
A specified method is not implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate required memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A pointer passed as a parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for unknown reasons.

</td>
</tr>
</table>
 




## -remarks



The NAT API with UPnP technology uses the combination of the external port and the protocol to identify the port mapping.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221069(v=VS.85).aspx">BSTR</a>



<a href="https://msdn.microsoft.com/5013fea2-e767-4600-a10c-6859b7be42e4">IStaticPortMapping</a>



<a href="https://msdn.microsoft.com/4858c474-b57e-4baa-8e82-10bc41e026cd">IStaticPortMappingCollection</a>



<a href="https://msdn.microsoft.com/bf14d633-4b91-4570-b4c9-fd524923914a">Network Address Translation Traversal Interfaces</a>



<a href="https://msdn.microsoft.com/49c5642e-346f-488d-92fb-ae214eb41b4f">Network Address Translation Traversal Reference</a>
 

 

