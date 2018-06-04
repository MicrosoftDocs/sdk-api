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

# IWdsTransportNamespaceScheduledCast interface


## -description


Represents a base interface to the derived interfaces: <a href="https://msdn.microsoft.com/ffbbdd4c-5d64-4ec0-a2f3-a5d31aec6402">IWdsTransportNamespaceScheduledCastManualStart</a> and <a href="https://msdn.microsoft.com/f11122a2-6ea9-4a73-ac93-0af7961f52b6">IWdsTransportNamespaceScheduledCastAutoStart</a>. An administrator must start  multicast sessions that are hosted by a namespace object of  these derived interfaces.   


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWdsTransportNamespaceScheduledCast</b> interface inherits from <a href="https://msdn.microsoft.com/eadb7b1b-aaef-4a4e-a2de-c641a4e10173">IWdsTransportNamespace</a>. <b>IWdsTransportNamespaceScheduledCast</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWdsTransportNamespaceScheduledCast</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/408ba96e-1a88-4a53-9cbe-8f2763542659">StartTransmission</a>
</td>
<td align="left" width="63%">
Starts a transmission on a namespace.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/eadb7b1b-aaef-4a4e-a2de-c641a4e10173">IWdsTransportNamespace</a>
 

 

