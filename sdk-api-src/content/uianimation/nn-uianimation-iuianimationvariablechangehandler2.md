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

# IUIAnimationVariableChangeHandler2 interface


## -description


Defines a method for handling animation variable update events. <b>IUIAnimationVariableChangeHandler2</b> handles events that occur in a specified dimension.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationVariableChangeHandler2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationVariableChangeHandler2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationVariableChangeHandler2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3C885518-8EAC-4123-83A5-5DEB27523DEF">OnValueChanged</a>
</td>
<td align="left" width="63%">

         Handles events that occur when the value of an animation variable changes in the specified dimension.

</td>
</tr>
</table> 


## -remarks




        The <a href="https://msdn.microsoft.com/3C885518-8EAC-4123-83A5-5DEB27523DEF">
         OnValueChanged</a> method receives animation variable value updates as 
         <b>DOUBLE</b> values.
      
         To receive value updates as <b>INT32</b> values, use
         the <a href="https://msdn.microsoft.com/76889784-BF1B-475B-8D84-201BEE6F0594">IUIAnimationVariableIntegerChangeHandler2::OnIntegerValueChanged</a> method.




## -see-also




<a href="https://msdn.microsoft.com/7925D462-C3FD-4BD2-806D-66FE822979EF">
         IUIAnimationVariable2::GetValue</a>



<a href="https://msdn.microsoft.com/F603C693-8F91-483F-8B0A-712E03BC10E5">IUIAnimationVariable2::SetVariableChangeHandler</a>



<a href="https://msdn.microsoft.com/778BE01B-360C-431C-9515-DE43B4F2B77D">IUIAnimationVariableIntegerChangeHandler2</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

