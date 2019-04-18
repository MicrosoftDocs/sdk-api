---
UID: NF:uiautomationclient.IUIAutomationValuePattern.get_CurrentValue
title: IUIAutomationValuePattern::get_CurrentValue (uiautomationclient.h)
author: windows-sdk-content
description: Retrieves the value of the element.
old-location: winauto\uiauto_IUIAutomationValuePattern_CurrentValue.htm
tech.root: WinAuto
ms.assetid: df7d4e74-34d1-435c-86cd-a8fee52f6a94
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CurrentValue property [Windows Accessibility], CurrentValue property [Windows Accessibility],IUIAutomationValuePattern interface, IUIAutomationValuePattern interface [Windows Accessibility],CurrentValue property, IUIAutomationValuePattern.CurrentValue, IUIAutomationValuePattern.get_CurrentValue, IUIAutomationValuePattern::CurrentValue, IUIAutomationValuePattern::get_CurrentValue, get_CurrentValue, uiauto.uiauto_IUIAutomationValuePattern_CurrentValue, uiauto_IUIAutomationValuePattern_CurrentValue, uiautomationclient/IUIAutomationValuePattern::CurrentValue, uiautomationclient/IUIAutomationValuePattern::get_CurrentValue, winauto.uiauto_IUIAutomationValuePattern_CurrentValue
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationValuePattern.CurrentValue
 - IUIAutomationValuePattern.get_CurrentValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationValuePattern::get_CurrentValue


## -description


Retrieves the value of the element.

This property is read-only.


## -parameters


## -remarks



Single-line edit controls support programmatic access to their contents through <a href="https://msdn.microsoft.com/07277405-1172-42e5-af51-8e2c1ea06894">IUIAutomationValuePattern</a>. However, multiline edit controls do not support this control pattern, and their contents must be retrieved by using <a href="https://msdn.microsoft.com/ddcf7ecd-7ed2-4b57-82a7-c7e1608dbfa1">IUIAutomationTextPattern</a>.

This property does not support the retrieval of formatting information or substring values. <a href="https://msdn.microsoft.com/ddcf7ecd-7ed2-4b57-82a7-c7e1608dbfa1">IUIAutomationTextPattern</a> must be used in these scenarios as well.




## -see-also




<a href="https://msdn.microsoft.com/07277405-1172-42e5-af51-8e2c1ea06894">IUIAutomationValuePattern</a>
 

 

