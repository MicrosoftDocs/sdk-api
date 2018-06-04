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

# IRemoteDesktopClientSettings interface


## -description


Provides the methods needed to configure the connection settings for the Remote Desktop Protocol (RDP) app container client control.

Use the <a href="https://msdn.microsoft.com/4b4c1080-3ea1-4557-92d6-45a80a788071">IRemoteDesktopClient</a>
<a href="https://msdn.microsoft.com/library/windows/hardware/mt168438">Settings</a> property to obtain a pointer to this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRemoteDesktopClientSettings</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IRemoteDesktopClientSettings</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRemoteDesktopClientSettings</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24f17f50-6cb0-422a-88c6-77bae48af392">ApplySettings</a>
</td>
<td align="left" width="63%">
Stores the specified contents in the RDP file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e172098a-d3c1-46cc-8c46-cdf14c46b43a">GetRdpProperty</a>
</td>
<td align="left" width="63%">
Retrieves a single named RDP property value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c28a172-42f3-4abd-9983-ee5acb1c9c78">RetrieveSettings</a>
</td>
<td align="left" width="63%">
Retrieves the entire RDP file as a string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c1a9e70-3e77-4f21-b3a1-8e4c3c5cf148">SetRdpProperty</a>
</td>
<td align="left" width="63%">
Sets the value of a single named RDP property.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/EAF75483-90A4-4BB1-82A5-EFBB2219A55B">Remote Desktop ActiveX control reference</a>
 

 

