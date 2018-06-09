---
UID: NN:natupnp.INATExternalIPAddressCallback
title: INATExternalIPAddressCallback
author: windows-sdk-content
description: The INATExternalIPAddressCallback interface is implemented by the NAT application with UPnP technology. It provides a method that the system calls if the external IP address of the NAT computer changes.
old-location: ics\inatexternalipaddresscallback.htm
old-project: ICS
ms.assetid: f180f597-680b-47ce-b437-3395069a8c77
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: INATExternalIPAddressCallback, INATExternalIPAddressCallback interface [ICS/ICF], INATExternalIPAddressCallback interface [ICS/ICF],described, _ics_inatexternalipaddresscallback, ics.inatexternalipaddresscallback, natupnp/INATExternalIPAddressCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - INATExternalIPAddressCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: Hnetcfg.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INATExternalIPAddressCallback interface


## -description


The 
<b>INATExternalIPAddressCallback</b> interface is implemented by the NAT application with UPnP technology. It provides a method that the system calls if the external IP address of the NAT computer changes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INATExternalIPAddressCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>INATExternalIPAddressCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INATExternalIPAddressCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b231ed4d-a115-4f4c-bda5-f6f3131ac45b">NewExternalIPAddress</a>
</td>
<td align="left" width="63%">
Notifies application when the NAT external address has changed.</p> (Inherited from <b>INATExternalIPAddressCallback</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/18c5df1a-e57e-4f44-bac5-a5861f939673">INATEventManager</a>



<a href="https://msdn.microsoft.com/c64e5ce3-78f6-4f51-8ae1-c871c4716d26">INATNumberOfEntriesCallback</a>



<a href="https://msdn.microsoft.com/bf14d633-4b91-4570-b4c9-fd524923914a">Network Address Translation Traversal Interfaces</a>



<a href="https://msdn.microsoft.com/49c5642e-346f-488d-92fb-ae214eb41b4f">Network Address Translation Traversal Reference</a>
 

 

