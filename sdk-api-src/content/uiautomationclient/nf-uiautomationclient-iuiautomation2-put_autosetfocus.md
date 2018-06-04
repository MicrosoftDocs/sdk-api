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

# IUIAutomation2::put_AutoSetFocus


## -description


Specifies whether calls to UI Automation control pattern methods automatically set focus to the target element.

This property is read/write.


## -parameters


## -remarks



 By default, most UI Automation methods that perform an action on an element, such as <a href="https://msdn.microsoft.com/dd04426c-edc5-4ee9-95ac-22f32fb14daa">IUIAutomationInvokePattern::Invoke</a> and <a href="https://msdn.microsoft.com/9b4caa59-bda4-4cc6-b2d8-ff47ea292746">IUIAutomationValuePattern::SetValue</a>, set focus to the element before performing the action. For most applications, setting the focus results in a more consistent user experience.  In situations where setting the focus would be disruptive, such as automating a drop-down menu, you can set <b>AutoSetFocus</b> to FALSE to prevent UI Automation methods from setting the focus. 




## -see-also




<a href="https://msdn.microsoft.com/45B4D41E-9C5C-47C7-86EB-D7B9BA14211B">IUIAutomation2</a>
 

 

