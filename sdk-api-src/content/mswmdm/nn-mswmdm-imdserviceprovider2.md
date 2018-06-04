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

# IMDServiceProvider2 interface


## -description



The <b>IMDServiceProvider2</b> interface extends the <a href="https://msdn.microsoft.com/803b6cc5-2cb2-42ad-a92c-05f098cbe8ae">IMDServiceProvider</a> interface by providing a way of obtaining <a href="https://msdn.microsoft.com/98f16547-4d8a-4422-ba08-c3c678142492">IMDSPDevice</a> object(s) for a given device path name. The device path name comes from the Plug and Play (PnP) subsystem.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDServiceProvider2</b> interface inherits from <a href="https://msdn.microsoft.com/803b6cc5-2cb2-42ad-a92c-05f098cbe8ae">IMDServiceProvider</a>. <b>IMDServiceProvider2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMDServiceProvider2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f724ef14-c572-41ca-a56b-fde85d7620e0">CreateDevice</a>
</td>
<td align="left" width="63%">
Creates devices by using the device path.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/803b6cc5-2cb2-42ad-a92c-05f098cbe8ae">IMDServiceProvider Interface</a>



<a href="https://msdn.microsoft.com/bd61c5fa-047c-4d93-bae1-f3433696b95b">Interfaces for Service Providers</a>
 

 

