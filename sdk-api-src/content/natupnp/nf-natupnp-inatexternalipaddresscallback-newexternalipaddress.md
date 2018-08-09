---
UID: NF:natupnp.INATExternalIPAddressCallback.NewExternalIPAddress
title: INATExternalIPAddressCallback::NewExternalIPAddress
author: windows-sdk-content
description: The system calls the NewExternalIPAddress method if the external IP address of the NAT computer changes.
old-location: ics\inatexternalipaddresscallback_newexternalipaddress.htm
old-project: ics
ms.assetid: b231ed4d-a115-4f4c-bda5-f6f3131ac45b
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: INATExternalIPAddressCallback interface [ICS/ICF],NewExternalIPAddress method, INATExternalIPAddressCallback.NewExternalIPAddress, INATExternalIPAddressCallback::NewExternalIPAddress, NewExternalIPAddress, NewExternalIPAddress method [ICS/ICF], NewExternalIPAddress method [ICS/ICF],INATExternalIPAddressCallback interface, _ics_inatexternalipaddresscallback_newexternalipaddress, ics.inatexternalipaddresscallback_newexternalipaddress, natupnp/INATExternalIPAddressCallback::NewExternalIPAddress
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
 - INATExternalIPAddressCallback.NewExternalIPAddress
product: Windows
targetos: Windows
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INATExternalIPAddressCallback::NewExternalIPAddress


## -description


The system calls the 
<b>NewExternalIPAddress</b> method if the external IP address of the NAT computer changes.


## -parameters




### -param bstrNewExternalIPAddress [in]

Specifies a 
<a href="https://msdn.microsoft.com/en-us/library/ms221069(v=VS.85).aspx">BSTR</a> variable that contains the new external IP address.


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



One reason why the external IP address of the NAT computer could change would be the IP address is allocated through DHCP, and the DHCP lease expired.




## -see-also




<a href="https://msdn.microsoft.com/5bc3e19c-3015-44fb-87a9-645e11283643">INATEventManager::put_ExternalIPAddressCallback</a>



<a href="https://msdn.microsoft.com/f180f597-680b-47ce-b437-3395069a8c77">INATExternalIPAddressCallback</a>



<a href="https://msdn.microsoft.com/bf14d633-4b91-4570-b4c9-fd524923914a">Network Address Translation Traversal Interfaces</a>



<a href="https://msdn.microsoft.com/49c5642e-346f-488d-92fb-ae214eb41b4f">Network Address Translation Traversal Reference</a>
 

 

