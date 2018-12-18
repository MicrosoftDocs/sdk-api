---
UID: NF:natupnp.IStaticPortMapping.get_InternalClient
title: IStaticPortMapping::get_InternalClient
author: windows-sdk-content
description: The get_InternalClient method retrieves the name of the internal client for this port mapping.
old-location: ics\istaticportmapping_get_internalclient.htm
tech.root: ics
ms.assetid: 91756e75-1915-4d61-841e-6a6cf1e849eb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IStaticPortMapping interface [ICS/ICF],get_InternalClient method, IStaticPortMapping.get_InternalClient, IStaticPortMapping::get_InternalClient, _ics_istaticportmapping_get_internalclient, get_InternalClient, get_InternalClient method [ICS/ICF], get_InternalClient method [ICS/ICF],IStaticPortMapping interface, ics.istaticportmapping_get_internalclient, natupnp/IStaticPortMapping::get_InternalClient
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
 - IStaticPortMapping.get_InternalClient
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStaticPortMapping::get_InternalClient


## -description


The 
<b>get_InternalClient</b> method retrieves the name of the internal client for this port mapping.


## -parameters




### -param pVal [out]

Pointer to a 
<a href="https://msdn.microsoft.com/en-us/library/ms221069(v=VS.85).aspx">BSTR</a> variable that receives the name of the internal client for this port mapping.


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



<a href="https://msdn.microsoft.com/864d0edf-c9fd-4ea0-b950-119dc4a630dc">IStaticPortMapping::EditInternalClient</a>



<a href="https://msdn.microsoft.com/bf14d633-4b91-4570-b4c9-fd524923914a">Network Address Translation Traversal Interfaces</a>



<a href="https://msdn.microsoft.com/49c5642e-346f-488d-92fb-ae214eb41b4f">Network Address Translation Traversal Reference</a>
 

 

