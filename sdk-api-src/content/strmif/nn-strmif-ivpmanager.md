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

# IVPManager interface


## -description



The <code>IVPManager</code> interface is implemented on the <a href="https://msdn.microsoft.com/d70558a5-9820-432a-b4f3-ccf7bb2a34d5">Video Port Manager</a> (VPM). The interface provides methods for applications to specify and retrieve indexes for ports when there are multiple video ports on a system, and to specify and retrieve the rectangle used by the video port. Currently, only the two index-related methods are implemented.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVPManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVPManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVPManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e30c2d7-b986-47f5-94c8-53937d1e1501">GetVideoPortIndex</a>
</td>
<td align="left" width="63%">
Returns the current video port index being used by the Video Port Manager.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a75332c9-ce3f-4122-ac6c-45478bb5f82c">SetVideoPortIndex</a>
</td>
<td align="left" width="63%">
Instructs the Video Port Manager to connect to the specified video port.

</td>
</tr>
</table> 

