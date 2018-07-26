---
UID: NF:uiautomationclient.IUIAutomationElement.get_CurrentControlType
title: IUIAutomationElement::get_CurrentControlType
author: windows-sdk-content
description: Retrieves the control type of the element.
old-location: winauto\uiauto_IUIAutomationElement_CurrentControlType.htm
old-project: WinAuto
ms.assetid: 6bceeabd-be77-4820-842a-d343fa2857bd
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: CurrentControlType property [Windows Accessibility], CurrentControlType property [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],CurrentControlType property, IUIAutomationElement.CurrentControlType, IUIAutomationElement.get_CurrentControlType, IUIAutomationElement::CurrentControlType, IUIAutomationElement::get_CurrentControlType, get_CurrentControlType, uiauto.uiauto_IUIAutomationElement_CurrentControlType, uiauto_IUIAutomationElement_CurrentControlType, uiautomationclient/IUIAutomationElement::CurrentControlType, uiautomationclient/IUIAutomationElement::get_CurrentControlType, winauto.uiauto_IUIAutomationElement_CurrentControlType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: "*UI_ANIMATION_KEYFRAME"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationElement.CurrentControlType
 - IUIAutomationElement.get_CurrentControlType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationElement::get_CurrentControlType


## -description


Retrieves the control type of the element.

This property is read-only.


## -parameters


## -remarks



Control types describe a known interaction model for UI Automation elements without relying on a localized control type or combination of complex logic rules.
This property cannot change at run time unless the control supports the <a href="https://msdn.microsoft.com/4a1613b9-1e64-4d4e-876e-e2bf886097d4">IUIAutomationMultipleViewPattern</a> interface. An example is the Win32 ListView control, which can change from a data grid to a list, depending on the current view.




## -see-also




<a href="https://msdn.microsoft.com/f7613ad1-0b75-46fb-b9ac-b1ae9eea4193">Automation Element Property IDs</a>



<a href="https://msdn.microsoft.com/48b232a8-8826-4c70-b541-3e6a792105c1">CachedControlType</a>



<a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>



<b>Reference</b>
 

 

