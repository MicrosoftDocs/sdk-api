---
UID: NF:natupnp.IStaticPortMapping.get_InternalPort
title: IStaticPortMapping::get_InternalPort
author: windows-driver-content
description: The get_InternalPort method retrieves the internal port on the client computer for this port mapping.
old-location: ics\istaticportmapping_get_internalport.htm
old-project: ICS
ms.assetid: 21b07be3-a838-4e7c-b521-100e2422f8b1
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: IStaticPortMapping interface [ICS/ICF],get_InternalPort method, IStaticPortMapping.get_InternalPort, IStaticPortMapping::get_InternalPort, _ics_istaticportmapping_get_internalport, get_InternalPort, get_InternalPort method [ICS/ICF], get_InternalPort method [ICS/ICF],IStaticPortMapping interface, ics.istaticportmapping_get_internalport, natupnp/IStaticPortMapping::get_InternalPort
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
-	IStaticPortMapping.get_InternalPort
product: Windows
targetos: Windows
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IStaticPortMapping::get_InternalPort


## -description


The <b>get_InternalPort</b> method retrieves the internal port on the client computer for this port mapping.


## -parameters




### -param pVal [out]

Pointer to a <b>long</b> variable that receives the internal port on the client computer for this port mapping.


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
 




## -see-also




<a href="https://msdn.microsoft.com/5013fea2-e767-4600-a10c-6859b7be42e4">IStaticPortMapping</a>



<a href="https://msdn.microsoft.com/8a43d828-327a-42be-8b8e-f3d669727fd7">IStaticPortMapping::EditInternalPort</a>



<a href="https://msdn.microsoft.com/bf14d633-4b91-4570-b4c9-fd524923914a">Network Address Translation Traversal Interfaces</a>



<a href="https://msdn.microsoft.com/49c5642e-346f-488d-92fb-ae214eb41b4f">Network Address Translation Traversal Reference</a>
 

 

