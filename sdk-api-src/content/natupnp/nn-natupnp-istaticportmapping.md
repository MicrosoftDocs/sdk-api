---
UID: NN:natupnp.IStaticPortMapping
title: IStaticPortMapping (natupnp.h)
author: windows-sdk-content
description: The IStaticPortMapping interface provides methods to retrieve and change the information for a particular port mapping.
old-location: ics\istaticportmapping.htm
tech.root: ics
ms.assetid: 5013fea2-e767-4600-a10c-6859b7be42e4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IStaticPortMapping, IStaticPortMapping interface [ICS/ICF], IStaticPortMapping interface [ICS/ICF],described, _ics_istaticportmapping, ics.istaticportmapping, natupnp/IStaticPortMapping
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
 - IStaticPortMapping
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStaticPortMapping interface


## -description


The 
<b>IStaticPortMapping</b> interface provides methods to retrieve and change the information for a particular port mapping.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStaticPortMapping</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IStaticPortMapping</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStaticPortMapping</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6bfa6242-298e-4835-9eda-fdc6a88d848f">EditDescription</a>
</td>
<td align="left" width="63%">
Changes the description for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/864d0edf-c9fd-4ea0-b950-119dc4a630dc">EditInternalClient</a>
</td>
<td align="left" width="63%">
Changes the internal client for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a43d828-327a-42be-8b8e-f3d669727fd7">EditInternalPort</a>
</td>
<td align="left" width="63%">
Changes the internal port for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66aa27b4-83a5-4c20-b964-084dd0e48a54">Enable</a>
</td>
<td align="left" width="63%">
Enables or disables this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b25fdff-8ad1-470f-bfd1-758f0bf8ea1f">get_Description</a>
</td>
<td align="left" width="63%">
Retrieves the description for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4a787ac-0ab2-413e-8738-23296e969477">get_Enabled</a>
</td>
<td align="left" width="63%">
Retrieves whether this port mapping is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4641f827-5408-4a4b-8454-41e960926621">get_ExternalIPAddress</a>
</td>
<td align="left" width="63%">
Retrieves the external IP address for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2a63d036-37d5-4686-a19e-11fd5dab6f64">get_ExternalPort</a>
</td>
<td align="left" width="63%">
Retrieves the external port for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/91756e75-1915-4d61-841e-6a6cf1e849eb">get_InternalClient</a>
</td>
<td align="left" width="63%">
Retrieves the name of the internal client for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/21b07be3-a838-4e7c-b521-100e2422f8b1">get_InternalPort</a>
</td>
<td align="left" width="63%">
Retrieves the internal port for this port mapping.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b9fc5ccc-43af-4dce-ba69-d11cdb4e3154">get_Protocol</a>
</td>
<td align="left" width="63%">
Retrieves the protocol for this port mapping.

</td>
</tr>
</table> 


## -remarks



The NAT API with UPnP technology uses the combination of the external port and the protocol to identify the port mapping.




## -see-also




<a href="https://msdn.microsoft.com/4858c474-b57e-4baa-8e82-10bc41e026cd">IStaticPortMappingCollection</a>



<a href="https://msdn.microsoft.com/bf14d633-4b91-4570-b4c9-fd524923914a">Network Address Translation Traversal Interfaces</a>



<a href="https://msdn.microsoft.com/49c5642e-346f-488d-92fb-ae214eb41b4f">Network Address Translation Traversal Reference</a>
 

 

