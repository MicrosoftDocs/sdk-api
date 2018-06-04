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

# IUIAnimationVariableCurveChangeHandler2 interface


## -description


Defines a method for handling animation curve update events. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationVariableCurveChangeHandler2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationVariableCurveChangeHandler2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationVariableCurveChangeHandler2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/CD0F59F7-9383-4602-8A97-356AEAB0FD82">OnCurveChanged</a>
</td>
<td align="left" width="63%">

         Handles events that occur when the animation curve of an animation variable changes.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/59E7C7A1-2461-487C-A263-A9DFC851B720">
         IUIAnimationVariable2::GetCurve</a>



<a href="https://msdn.microsoft.com/CAC7D415-5B0F-4587-8F1C-65399D2A5A58">
         IUIAnimationVariable2::GetVectorCurve</a>



<a href="https://msdn.microsoft.com/98C95C85-30C9-4E3E-82FE-E3D4C7ECAE0B">IUIAnimationVariable2::SetVariableCurveChangeHandler </a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

