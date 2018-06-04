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

# IRDPSRAPIPerfCounterLogger interface


## -description


Enables a client application to implement custom performance logging.

Applications obtain access to this object using the <a href="https://msdn.microsoft.com/611ABFB6-851F-4A2C-86A0-E26732CD20BE">IRDPSRAPIPerfCounterLoggingManager</a><b>::</b><a href="https://msdn.microsoft.com/24C57AE8-208B-4254-B5B1-8AB77E2D4044">CreateLogger</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRDPSRAPIPerfCounterLogger</b> class inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRDPSRAPIPerfCounterLogger</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRDPSRAPIPerfCounterLogger</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B6EF608E-5AA9-4AB7-920D-F6E567E1258C">LogValue</a>
</td>
<td align="left" width="63%">
Logs a value.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/bb1df622-bfcd-4d84-b5f6-780b693cc760">Windows Desktop Sharing Interfaces</a>
 

 

