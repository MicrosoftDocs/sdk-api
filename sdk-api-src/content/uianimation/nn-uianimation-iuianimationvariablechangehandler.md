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

# IUIAnimationVariableChangeHandler interface


## -description



      Defines a method for handling events related to animation variable updates.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIAnimationVariableChangeHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIAnimationVariableChangeHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIAnimationVariableChangeHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e865f55-d703-4d91-8690-b816b5fe1a89">
         OnValueChanged</a>
</td>
<td align="left" width="63%">

         Handles events that occur when the value of an animation variable changes.

</td>
</tr>
</table> 


## -remarks




<a href="https://msdn.microsoft.com/1e865f55-d703-4d91-8690-b816b5fe1a89">
         OnValueChanged</a> receives animation variable value updates as 
         <b>DOUBLE</b> values.
      
         To receive value updates as <b>INT32</b> values, use
         <a href="https://msdn.microsoft.com/e12224a2-c8f3-45eb-a254-d624de16e12d">IUIAnimationVariableIntegerChangeHandler::OnIntegerValueChanged</a>.




## -see-also




<a href="https://msdn.microsoft.com/51ae200a-a630-44fd-afd4-33d1b1dbf6d7">
         IUIAnimationVariable::GetValue</a>



<a href="https://msdn.microsoft.com/d773a59f-10a5-41e4-92f1-af72d8d15105">IUIAnimationVariable::SetVariableChangeHandler</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

