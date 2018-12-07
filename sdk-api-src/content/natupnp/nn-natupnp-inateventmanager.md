---
UID: NN:natupnp.INATEventManager
title: INATEventManager
author: windows-sdk-content
description: The INATEventManager interface provides methods for NAT applications with UPnP technology to register callback interfaces with the NAT. The system calls the methods in these interfaces when the configuration of the NAT changes.
old-location: ics\inateventmanager.htm
tech.root: ics
ms.assetid: 18c5df1a-e57e-4f44-bac5-a5861f939673
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: INATEventManager, INATEventManager interface [ICS/ICF], INATEventManager interface [ICS/ICF],described, _ics_inateventmanager, ics.inateventmanager, natupnp/INATEventManager
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - INATEventManager
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INATEventManager interface


## -description


The 
<b>INATEventManager</b> interface provides methods for NAT applications with UPnP technology to register callback interfaces with the NAT. The system calls the methods in these interfaces when the configuration of the NAT changes.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INATEventManager</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>INATEventManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INATEventManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5bc3e19c-3015-44fb-87a9-645e11283643">put_ExternalIPAddressCallback</a>
</td>
<td align="left" width="63%">
Registers the 
<a href="https://msdn.microsoft.com/f180f597-680b-47ce-b437-3395069a8c77">INATExternalIPAddressCallback</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a02a0f1e-5085-444b-adc4-c3cd919f7e25">put_NumberOfEntriesCallback</a>
</td>
<td align="left" width="63%">
Registers the 
<a href="https://msdn.microsoft.com/c64e5ce3-78f6-4f51-8ae1-c871c4716d26">INATNumberOfEntriesCallback</a> interface.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/bf14d633-4b91-4570-b4c9-fd524923914a">Network Address Translation Traversal Interfaces</a>



<a href="https://msdn.microsoft.com/49c5642e-346f-488d-92fb-ae214eb41b4f">Network Address Translation Traversal Reference</a>
 

 

