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

# IUIAnimationVariableIntegerChangeHandler interface


## -description



      Defines a method for handling animation variable update events.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationVariableIntegerChangeHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationVariableIntegerChangeHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationVariableIntegerChangeHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e12224a2-c8f3-45eb-a254-d624de16e12d">
         OnIntegerValueChanged</a>
</td>
<td align="left" width="63%">

         Handles events that occur when the value of an animation variable changes.

</td>
</tr>
</table> 


## -remarks




<a href="https://msdn.microsoft.com/e12224a2-c8f3-45eb-a254-d624de16e12d">
         OnIntegerValueChanged</a> receives animation variable value updates as <b>INT32</b> values.
      
         To receive value updates as <b>DOUBLE</b> values, use
         the <a href="https://msdn.microsoft.com/1e865f55-d703-4d91-8690-b816b5fe1a89">IUIAnimationVariableChangeHandler::OnValueChanged</a> method.




## -see-also




<a href="https://msdn.microsoft.com/044fd6a3-6e40-4f4f-8777-1a1a66c91989">
         IUIAnimationVariable::GetIntegerValue</a>



<a href="https://msdn.microsoft.com/8dc20701-0808-4308-92fc-8be6c4b039ca">IUIAnimationVariable::SetVariableIntegerChangeHandler</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

