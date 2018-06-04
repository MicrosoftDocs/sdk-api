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

# IWTSListener interface


## -description


Manages configuration settings for each listener for the dynamic virtual channel (DVC) connection.

This interface is implemented by the Remote Desktop Connection (RDC) client. A reference is kept typically by the Remote Desktop Connection (RDC) client plug-in. The methods can be executed in any thread that the plug-in chooses. An instance is retrieved by calling the <a href="https://msdn.microsoft.com/62800999-bd13-4529-b5e4-5c6d67d3a6bc">IWTSVirtualChannelManager::CreateListener</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWTSListener</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWTSListener</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWTSListener</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d45ab39-0a65-4424-b6ea-2a54bb063c0f">GetConfiguration</a>
</td>
<td align="left" width="63%">
Retrieves the listener-specific configuration.

</td>
</tr>
</table> 

