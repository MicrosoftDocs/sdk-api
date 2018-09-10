---
UID: NF:uiautomationclient.IUIAutomationRangeValuePattern.get_CurrentLargeChange
title: IUIAutomationRangeValuePattern::get_CurrentLargeChange
author: windows-sdk-content
description: Retrieves the value that is added to or subtracted from the value of the control when a large change is made, such as when the PAGE DOWN key is pressed.
old-location: winauto\uiauto_IUIAutomationRangeValuePattern_CurrentLargeChange.htm
tech.root: WinAuto
ms.assetid: 801d7a2c-387f-4770-980a-fc5fb98959d8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CurrentLargeChange property [Windows Accessibility], CurrentLargeChange property [Windows Accessibility],IUIAutomationRangeValuePattern interface, IUIAutomationRangeValuePattern interface [Windows Accessibility],CurrentLargeChange property, IUIAutomationRangeValuePattern.CurrentLargeChange, IUIAutomationRangeValuePattern.get_CurrentLargeChange, IUIAutomationRangeValuePattern::CurrentLargeChange, IUIAutomationRangeValuePattern::get_CurrentLargeChange, get_CurrentLargeChange, uiauto.uiauto_IUIAutomationRangeValuePattern_CurrentLargeChange, uiauto_IUIAutomationRangeValuePattern_CurrentLargeChange, uiautomationclient/IUIAutomationRangeValuePattern::CurrentLargeChange, uiautomationclient/IUIAutomationRangeValuePattern::get_CurrentLargeChange, winauto.uiauto_IUIAutomationRangeValuePattern_CurrentLargeChange
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
 - IUIAutomationRangeValuePattern.CurrentLargeChange
 - IUIAutomationRangeValuePattern.get_CurrentLargeChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationRangeValuePattern::get_CurrentLargeChange


## -description


Retrieves the value that is added to or subtracted from the value of the control when a large change is made, such as when the PAGE DOWN key is pressed.

This property is read-only.


## -parameters


## -remarks



The LargeChange property can support a Not a Number (NaN) value. When retrieving this property, a client can use the <a href="http://go.microsoft.com/fwlink/p/?linkid=198403">_isnan</a> function to determine whether the property is a NaN value.
        




## -see-also




<a href="https://msdn.microsoft.com/145c14e5-1b6b-4eb1-a73a-aa59b5e1b4c4">IUIAutomationRangeValuePattern</a>



<a href="https://msdn.microsoft.com/88de76d5-100c-41b9-b87e-2d1c3bf6e633">IUIAutomationRangeValuePattern::CurrentSmallChange</a>
 

 

