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

# IFindReferenceTargetsCallback interface


## -description


Defines the interface for callbacks from <a href="https://msdn.microsoft.com/ede8da3a-cef8-4741-950d-4303870ab10e">IReferenceTracker::FindTrackerTargets</a>. The implementation of this interface must pass any <a href="https://msdn.microsoft.com/204c647d-65c0-4b0e-b0fa-1abe9e8fdedd">IReferenceTrackerTarget</a> instances it finds to the <a href="https://msdn.microsoft.com/f8959af6-a857-4bca-a469-d68f70e2fadf">FoundTrackerTarget</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFindReferenceTargetsCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFindReferenceTargetsCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFindReferenceTargetsCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8959af6-a857-4bca-a469-d68f70e2fadf">FoundTrackerTarget</a>
</td>
<td align="left" width="63%">
Called whenever a XAML object reference tracker target is found.

</td>
</tr>
</table> 

