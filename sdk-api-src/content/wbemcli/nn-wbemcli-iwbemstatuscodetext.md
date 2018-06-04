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

# IWbemStatusCodeText interface


## -description


The 
<b>IWbemStatusCodeText</b> interface extracts text string descriptions of error codes or the name of the subsystem where the error occurred.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemStatusCodeText</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWbemStatusCodeText</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemStatusCodeText</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2adc740-f1d9-434e-a7ac-b4830350e862">GetErrorCodeText</a>
</td>
<td align="left" width="63%">
Returns the text string description associated with the error code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/831f8eb4-3dcd-42ec-aa43-309360e9a5ce">GetFacilityCodeText</a>
</td>
<td align="left" width="63%">
Returns the name of the subsystem where the error occurred.

</td>
</tr>
</table> 

