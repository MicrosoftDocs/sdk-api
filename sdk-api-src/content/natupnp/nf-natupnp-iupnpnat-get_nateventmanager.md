---
UID: NF:natupnp.IUPnPNAT.get_NATEventManager
title: IUPnPNAT::get_NATEventManager method
author: windows-driver-content
description: The get_NATEventManager method retrieves an INATEventManager interface for the NAT used by the local computer.
old-location: ics\iupnpnat_get_nateventmanager.htm
old-project: ICS
ms.assetid: 594fdd40-062e-4f81-af11-4170a5870472
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: IUPnPNAT, IUPnPNAT interface [ICS/ICF], get_NATEventManager method, IUPnPNAT::get_NATEventManager, _ics_iupnpnat_get_nateventmanager, get_NATEventManager method [ICS/ICF], get_NATEventManager method [ICS/ICF], IUPnPNAT interface, get_NATEventManager,IUPnPNAT.get_NATEventManager, ics.iupnpnat_get_nateventmanager, natupnp/IUPnPNAT::get_NATEventManager
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
-	IUPnPNAT.get_NATEventManager
product: Windows
targetos: Windows
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IUPnPNAT::get_NATEventManager method


## -description


The 
<b>get_NATEventManager</b> method retrieves an INATEventManager interface for the NAT used by the local computer.


## -parameters




### -param ppNEM [out]

Pointer to an interface pointer that points to an 
<a href="https://msdn.microsoft.com/18c5df1a-e57e-4f44-bac5-a5861f939673">INATEventManager</a> interface.


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




<a href="https://msdn.microsoft.com/18c5df1a-e57e-4f44-bac5-a5861f939673">INATEventManager</a>



<a href="https://msdn.microsoft.com/bfd93967-a514-4301-9b1e-0fee8794d929">IUPnPNAT</a>



<a href="https://msdn.microsoft.com/bf14d633-4b91-4570-b4c9-fd524923914a">Network Address Translation Traversal Interfaces</a>



<a href="https://msdn.microsoft.com/49c5642e-346f-488d-92fb-ae214eb41b4f">Network Address Translation Traversal Reference</a>
 

 

