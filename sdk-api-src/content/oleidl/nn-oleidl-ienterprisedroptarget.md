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

# IEnterpriseDropTarget interface


## -description


When implemented by the drop target application, this interface gives the OLE drag and drop engine the ability to determine whether the drop target application intends to evaluate enterprise protection policy and gives the OLE drag and drop engine a way to provide the enterprise ID of the drop source application to the drop target application.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnterpriseDropTarget</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IEnterpriseDropTarget</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnterpriseDropTarget</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EB28FF02-E747-4898-AEEF-811BAF7A6DBC">IsEvaluatingEdpPolicy</a>
</td>
<td align="left" width="63%">
Indicates whether the drop target is evaluating the enterprise protection policy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FFC64D7F-CBEA-4913-93B2-F19F4D0EA81E">SetDropSourceEnterpriseid</a>
</td>
<td align="left" width="63%">
Provides the drop target with the enterprise ID of the drop source.

</td>
</tr>
</table> 

