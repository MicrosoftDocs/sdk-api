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

# IRadialControllerInterop interface


## -description


Enables interoperability with a Universal Windows Platform (UWP) <a href="https://msdn.microsoft.com/5cd9534d-bdd7-49fa-81c7-a5ddca4e851a">RadialController</a> object and provides access to <b>RadialController</b> members for customizing the interaction experience.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRadialControllerInterop</b> interface inherits from <b>IInspectable</b>. <b>IRadialControllerInterop</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRadialControllerInterop</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe419ce2-9767-42c4-aaa6-a9b9ea93ec3e">CreateForWindow</a>
</td>
<td align="left" width="63%">
Instantiates a <a href="https://msdn.microsoft.com/5cd9534d-bdd7-49fa-81c7-a5ddca4e851a">RadialController</a> object and binds it to the active application.

</td>
</tr>
</table> 


## -see-also




<b>Developer and UX guidance</b>



<a href="https://msdn.microsoft.com/44FED16E-63FB-466B-9615-8B744F861AE9">Radial controller interfaces</a>



<b>Samples</b>



<a href="https://go.microsoft.com/fwlink/?linkid=832322">Surface Dial interactions</a>



<a href="https://go.microsoft.com/fwlink/?linkid=832713">Universal Windows Platform samples (C# and C++)</a>



<a href="https://aka.ms/radialcontrollerclassicsample">Windows classic desktop sample</a>
 

 

