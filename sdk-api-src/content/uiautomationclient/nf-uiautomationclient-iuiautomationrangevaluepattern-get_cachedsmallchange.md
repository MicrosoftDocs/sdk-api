---
UID: NF:uiautomationclient.IUIAutomationRangeValuePattern.get_CachedSmallChange
title: IUIAutomationRangeValuePattern::get_CachedSmallChange (uiautomationclient.h)
author: windows-sdk-content
description: Retrieves, from the cache, the value that is added to or subtracted from the value of the control when a small change is made, such as when an arrow key is pressed.
old-location: winauto\uiauto_IUIAutomationRangeValuePattern_CachedSmallChange.htm
tech.root: WinAuto
ms.assetid: 8d737eaa-eb4a-4d73-b515-876961423fd6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CachedSmallChange property [Windows Accessibility], CachedSmallChange property [Windows Accessibility],IUIAutomationRangeValuePattern interface, IUIAutomationRangeValuePattern interface [Windows Accessibility],CachedSmallChange property, IUIAutomationRangeValuePattern.CachedSmallChange, IUIAutomationRangeValuePattern.get_CachedSmallChange, IUIAutomationRangeValuePattern::CachedSmallChange, IUIAutomationRangeValuePattern::get_CachedSmallChange, get_CachedSmallChange, uiauto.uiauto_IUIAutomationRangeValuePattern_CachedSmallChange, uiauto_IUIAutomationRangeValuePattern_CachedSmallChange, uiautomationclient/IUIAutomationRangeValuePattern::CachedSmallChange, uiautomationclient/IUIAutomationRangeValuePattern::get_CachedSmallChange, winauto.uiauto_IUIAutomationRangeValuePattern_CachedSmallChange
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
 - IUIAutomationRangeValuePattern.CachedSmallChange
 - IUIAutomationRangeValuePattern.get_CachedSmallChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationRangeValuePattern::get_CachedSmallChange


## -description


Retrieves, from the cache, the value that is added to or subtracted from the value of the control when a small change is made, such as when an arrow key is pressed.

This property is read-only.


## -parameters


## -remarks



The SmallChange property can support a Not a Number (NaN) value. When retrieving this property, a client can use the <a href="https://go.microsoft.com/fwlink/p/?linkid=198403">_isnan</a> function to determine whether the property is a NaN value.
        




## -see-also




<a href="https://msdn.microsoft.com/145c14e5-1b6b-4eb1-a73a-aa59b5e1b4c4">IUIAutomationRangeValuePattern</a>



<a href="https://msdn.microsoft.com/d97addfd-53ae-4445-9f77-d24d97644bfc">IUIAutomationRangeValuePattern::CachedLargeChange</a>
 

 

