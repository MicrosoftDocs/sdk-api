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

# IInitiateWinSATAssessment interface


## -description


<p class="CCE_Message">[IInitiateWinSATAssessment may be altered or unavailable for releases after Windows 8.1.]

Initiates an assessment.

To retrieve this interface, call the <a href="_com_cocreateinstance">CoCreateInstance</a> function. Use __uuidof(CInitiateWinSAT) as the class identifier and __uuidof(IInitiateWinSATAssessment) as the interface identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInitiateWinSATAssessment</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IInitiateWinSATAssessment</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInitiateWinSATAssessment</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa4b159f-9d40-445f-bd43-5fc2e7b2d33b">CancelAssessment</a>
</td>
<td align="left" width="63%">
Cancels a currently running assessment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c57d88b6-81ac-4314-8593-59a950348be4">InitiateAssessment</a>
</td>
<td align="left" width="63%">
Initiates an ad hoc assessment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9425e41c-fe03-4c94-a5eb-686775b5fce7">InitiateFormalAssessment</a>
</td>
<td align="left" width="63%">
Initiates a formal assessment.

</td>
</tr>
</table> 

