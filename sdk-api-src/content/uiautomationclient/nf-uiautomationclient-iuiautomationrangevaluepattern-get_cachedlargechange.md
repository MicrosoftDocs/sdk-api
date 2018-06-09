---
UID: NF:uiautomationclient.IUIAutomationRangeValuePattern.get_CachedLargeChange
title: IUIAutomationRangeValuePattern::get_CachedLargeChange
author: windows-sdk-content
description: Retrieves, from the cache, the value that is added to or subtracted from the value of the control when a large change is made, such as when the PAGE DOWN key is pressed.
old-location: winauto\uiauto_IUIAutomationRangeValuePattern_CachedLargeChange.htm
old-project: WinAuto
ms.assetid: d97addfd-53ae-4445-9f77-d24d97644bfc
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: CachedLargeChange property [Windows Accessibility], CachedLargeChange property [Windows Accessibility],IUIAutomationRangeValuePattern interface, IUIAutomationRangeValuePattern interface [Windows Accessibility],CachedLargeChange property, IUIAutomationRangeValuePattern.CachedLargeChange, IUIAutomationRangeValuePattern.get_CachedLargeChange, IUIAutomationRangeValuePattern::CachedLargeChange, IUIAutomationRangeValuePattern::get_CachedLargeChange, get_CachedLargeChange, uiauto.uiauto_IUIAutomationRangeValuePattern_CachedLargeChange, uiauto_IUIAutomationRangeValuePattern_CachedLargeChange, uiautomationclient/IUIAutomationRangeValuePattern::CachedLargeChange, uiautomationclient/IUIAutomationRangeValuePattern::get_CachedLargeChange, winauto.uiauto_IUIAutomationRangeValuePattern_CachedLargeChange
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationRangeValuePattern.CachedLargeChange
 - IUIAutomationRangeValuePattern.get_CachedLargeChange
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationRangeValuePattern::get_CachedLargeChange


## -description


Retrieves, from the cache, the value that is added to or subtracted from the value of the control when a large change is made, such as when the PAGE DOWN key is pressed.

This property is read-only.


## -parameters


## -remarks



The LargeChange property can support a Not a Number (NaN) value. When retrieving this property, a client can use the <a href="http://go.microsoft.com/fwlink/p/?linkid=198403">_isnan</a> function to determine whether the property is a NaN value.
        




## -see-also




<a href="https://msdn.microsoft.com/145c14e5-1b6b-4eb1-a73a-aa59b5e1b4c4">IUIAutomationRangeValuePattern</a>



<a href="https://msdn.microsoft.com/8d737eaa-eb4a-4d73-b515-876961423fd6">IUIAutomationRangeValuePattern::CachedSmallChange</a>
 

 

