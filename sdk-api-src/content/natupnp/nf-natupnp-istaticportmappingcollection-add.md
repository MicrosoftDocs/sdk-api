---
UID: NF:natupnp.IStaticPortMappingCollection.Add
title: IStaticPortMappingCollection::Add
author: windows-driver-content
description: The Add method creates a new port mapping and adds it to the collection.
old-location: ics\istaticportmappingcollection_add.htm
old-project: ICS
ms.assetid: 5e61629d-80e4-4d44-8e53-12e17b399126
ms.author: windowsdriverdev
ms.date: 5/11/2018
ms.keywords: Add, Add method [ICS/ICF], Add method [ICS/ICF],IStaticPortMappingCollection interface, IStaticPortMappingCollection interface [ICS/ICF],Add method, IStaticPortMappingCollection.Add, IStaticPortMappingCollection::Add, _ics_istaticportmappingcollection_add, ics.istaticportmappingcollection_add, natupnp/IStaticPortMappingCollection::Add
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
req.typenames: SystemHealthAgentState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Hnetcfg.dll
api_name:
-	IStaticPortMappingCollection.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IStaticPortMappingCollection::Add


## -description


The 
<b>Add</b> method creates a new port mapping and adds it to the collection.


## -parameters




### -param lExternalPort [in]

Specifies the external port for this port mapping.


### -param bstrProtocol [in]

Specifies the protocol. This parameter should be either UDP or TCP.


### -param lInternalPort [in]

Specifies the internal port for this port mapping.


### -param bstrInternalClient [in]

Specifies the name of the client on the private network that uses this port mapping.


### -param bEnabled [in]

Specifies whether the port is 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn966102">enabled</a>.


### -param bstrDescription [in]

Specifies a description for this port mapping.


### -param ppSPM [out]

Pointer to an interface pointer that, on successful return, receives a pointer to an 
<a href="https://msdn.microsoft.com/5013fea2-e767-4600-a10c-6859b7be42e4">IStaticPortMapping</a> interface.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

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




<a href="https://msdn.microsoft.com/5013fea2-e767-4600-a10c-6859b7be42e4">IStaticPortMapping</a>



<a href="https://msdn.microsoft.com/4858c474-b57e-4baa-8e82-10bc41e026cd">IStaticPortMappingCollection</a>



<a href="https://msdn.microsoft.com/c82a145d-7b85-419b-b64b-36f1ac7a2631">IStaticPortMappingCollection::Remove</a>



<a href="https://msdn.microsoft.com/bf14d633-4b91-4570-b4c9-fd524923914a">Network Address Translation Traversal Interfaces</a>



<a href="https://msdn.microsoft.com/49c5642e-346f-488d-92fb-ae214eb41b4f">Network Address Translation Traversal Reference</a>
 

 

