---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IDot11AdHocManager interface


## -description


The <b>IDot11AdHocManager</b> interface creates and manages 802.11 ad hoc networks.  It is the top-level 802.11 ad hoc interface and the only ad hoc interface with a coclass. As such, it is the only ad hoc interface that can be instantiated by <a href="_com_CoCreateInstance">CoCreateInstance</a>. 
<div class="alert"><b>Note</b>  Ad hoc mode might not be available in future versions of Windows. Starting with Windows 8.1 and Windows Server 2012 R2, use <a href="https://msdn.microsoft.com/library/windows/hardware/mt244265">Wi-Fi Direct</a> instead.</div><div> </div>The <b>IDot11AdHocManager</b> coclass implements the <a href="_com_IConnectionPoint">IConnectionPoint</a> interface. The <a href="_com_IConnectionPoint_Advise">Advise</a> method can be used to register for network manager, network, and interface-related notifications. Notifications are implemented by the <a href="https://msdn.microsoft.com/a79931ad-deeb-4e46-a051-80a57fe5935c">IDot11AdHocManagerNotificationSink</a> interface. To register for notifications, call the <b>Advise</b> method with the appropriate notification sink interface as the <i>pUnk</i>  parameter.  


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDot11AdHocManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDot11AdHocManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDot11AdHocManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45beb340-1c19-4b91-8e5c-8849e690e988">IDot11AdHocManager::CommitCreatedNetwork</a>
</td>
<td align="left" width="63%">
Initializes a created network and optionally commits the network's profile to the profile store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d9930b3-7bc4-4015-b096-a21fe01f54f5">IDot11AdHocManager::CreateNetwork</a>
</td>
<td align="left" width="63%">
Creates a wireless ad hoc network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e705533-3657-4997-ae84-e18defbbc02a">IDot11AdHocManager::GetIEnumDot11AdHocInterfaces</a>
</td>
<td align="left" width="63%">
Returns the set of wireless network interface cards (NICs) available on the machine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d37fad8-18e8-4280-9fa8-e40c742ec8ba">IDot11AdHocManager::GetIEnumDot11AdHocNetworks</a>
</td>
<td align="left" width="63%">
Returns a list of available ad hoc network destinations within connection range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/971703dc-1a3c-4c9a-a9e2-c547c96beacd">IDot11AdHocManager::GetNetwork</a>
</td>
<td align="left" width="63%">
Returns the network associated with a signature. 

</td>
</tr>
</table> 

