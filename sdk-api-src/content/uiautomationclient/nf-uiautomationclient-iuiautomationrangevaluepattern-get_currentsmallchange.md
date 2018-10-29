---
UID: NF:uiautomationclient.IUIAutomationRangeValuePattern.get_CurrentSmallChange
title: IUIAutomationRangeValuePattern::get_CurrentSmallChange
author: windows-sdk-content
description: Retrieves the value that is added to or subtracted from the value of the control when a small change is made, such as when an arrow key is pressed.
old-location: winauto\uiauto_IUIAutomationRangeValuePattern_CurrentSmallChange.htm
tech.root: WinAuto
ms.assetid: 88de76d5-100c-41b9-b87e-2d1c3bf6e633
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: CurrentSmallChange property [Windows Accessibility], CurrentSmallChange property [Windows Accessibility],IUIAutomationRangeValuePattern interface, IUIAutomationRangeValuePattern interface [Windows Accessibility],CurrentSmallChange property, IUIAutomationRangeValuePattern.CurrentSmallChange, IUIAutomationRangeValuePattern.get_CurrentSmallChange, IUIAutomationRangeValuePattern::CurrentSmallChange, IUIAutomationRangeValuePattern::get_CurrentSmallChange, get_CurrentSmallChange, uiauto.uiauto_IUIAutomationRangeValuePattern_CurrentSmallChange, uiauto_IUIAutomationRangeValuePattern_CurrentSmallChange, uiautomationclient/IUIAutomationRangeValuePattern::CurrentSmallChange, uiautomationclient/IUIAutomationRangeValuePattern::get_CurrentSmallChange, winauto.uiauto_IUIAutomationRangeValuePattern_CurrentSmallChange
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IUIAutomationRangeValuePattern.CurrentSmallChange
 - IUIAutomationRangeValuePattern.get_CurrentSmallChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationRangeValuePattern::get_CurrentSmallChange


## -description


Retrieves the value that is added to or subtracted from the value of the control when a small change is made, such as when an arrow key is pressed.

This property is read-only.


## -parameters


## -remarks



The SmallChange property can support a Not a Number (NaN) value. When retrieving this property, a client can use the <a href="https://go.microsoft.com/fwlink/p/?linkid=198403">_isnan</a> function to determine whether the property is a NaN value.
        




## -see-also




<a href="https://msdn.microsoft.com/145c14e5-1b6b-4eb1-a73a-aa59b5e1b4c4">IUIAutomationRangeValuePattern</a>



<a href="https://msdn.microsoft.com/801d7a2c-387f-4770-980a-fc5fb98959d8">IUIAutomationRangeValuePattern::CurrentLargeChange</a>
 

 

