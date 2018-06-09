---
UID: NF:natupnp.IStaticPortMapping.get_Protocol
title: IStaticPortMapping::get_Protocol
author: windows-sdk-content
description: The get_Protocol method retrieves the protocol associated with this port mapping.
old-location: ics\istaticportmapping_get_protocol.htm
old-project: ICS
ms.assetid: b9fc5ccc-43af-4dce-ba69-d11cdb4e3154
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: IStaticPortMapping interface [ICS/ICF],get_Protocol method, IStaticPortMapping.get_Protocol, IStaticPortMapping::get_Protocol, _ics_istaticportmapping_get_protocol, get_Protocol, get_Protocol method [ICS/ICF], get_Protocol method [ICS/ICF],IStaticPortMapping interface, ics.istaticportmapping_get_protocol, natupnp/IStaticPortMapping::get_Protocol
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SystemHealthAgentState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Hnetcfg.dll
api_name:
 - IStaticPortMapping.get_Protocol
product: Windows
targetos: Windows
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IStaticPortMapping::get_Protocol


## -description


The 
<b>get_Protocol</b> method retrieves the protocol associated with this port mapping.


## -parameters




### -param pVal [out]

Pointer to a 
<a href="1b2d7d2c-47af-4389-a6b6-b01b7e915228">BSTR</a> variable that, receives the protocol for this port mapping. The protocol is either "UDP" or "TCP".


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



<a href="https://msdn.microsoft.com/bf14d633-4b91-4570-b4c9-fd524923914a">Network Address Translation Traversal Interfaces</a>



<a href="https://msdn.microsoft.com/49c5642e-346f-488d-92fb-ae214eb41b4f">Network Address Translation Traversal Reference</a>
 

 

