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

# IDirectManipulationViewport2 interface


## -description


Provides management of behaviors on a viewport. A behavior affects the functionality of a particular part of the <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> workflow. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectManipulationViewport2</b> interface inherits from <a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>. <b>IDirectManipulationViewport2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectManipulationViewport2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E65CF2A3-EF44-4B4E-A8C5-7DC75345B5A6">AddBehavior</a>
</td>
<td align="left" width="63%">
Adds a behavior to the viewport and returns a cookie to the caller.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94CCF2F4-F6E7-4446-8F6A-3E058B98A328">RemoveAllBehaviors</a>
</td>
<td align="left" width="63%">
Removes all behaviors added to the viewport.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CA5FF0FC-6ED9-4964-9751-90387650A198">RemoveBehavior</a>
</td>
<td align="left" width="63%">
Removes a behavior from the viewport that matches the given cookie.

</td>
</tr>
</table> 


## -remarks



<b>IDirectManipulationViewport2</b> can be used in place of <a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>.


Behaviors are created using <a href="https://msdn.microsoft.com/094C6C7D-F973-45AC-9B83-43DB9D46AF23">IDirectManipulationManager2</a> and an appropriate class ID.

A behavior can be attached or removed at any time and takes effect immediately (even during an active manipulation or inertia animation).




## -see-also




<a href="https://msdn.microsoft.com/03680CE5-A858-4876-B41C-6F2E08C02C22">Direct Manipulation Interfaces</a>



<a href="https://msdn.microsoft.com/4c14143b-3b5f-401d-9df7-f17374abcd99">IDirectManipulationViewport</a>
 

 

