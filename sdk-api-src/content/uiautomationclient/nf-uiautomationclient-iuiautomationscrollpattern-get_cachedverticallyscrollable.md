---
UID: NF:uiautomationclient.IUIAutomationScrollPattern.get_CachedVerticallyScrollable
title: IUIAutomationScrollPattern::get_CachedVerticallyScrollable
author: windows-sdk-content
description: Retrieves a cached value that indicates whether the element can scroll vertically.
old-location: winauto\uiauto_IUIAutomationScrollPattern_CachedVerticallyScrollable.htm
tech.root: WinAuto
ms.assetid: e9e55853-6fe3-4e51-bb4c-aea0174ed710
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CachedVerticallyScrollable property [Windows Accessibility], CachedVerticallyScrollable property [Windows Accessibility],IUIAutomationScrollPattern interface, IUIAutomationScrollPattern interface [Windows Accessibility],CachedVerticallyScrollable property, IUIAutomationScrollPattern.CachedVerticallyScrollable, IUIAutomationScrollPattern.get_CachedVerticallyScrollable, IUIAutomationScrollPattern::CachedVerticallyScrollable, IUIAutomationScrollPattern::get_CachedVerticallyScrollable, get_CachedVerticallyScrollable, uiauto.uiauto_IUIAutomationScrollPattern_CachedVerticallyScrollable, uiauto_IUIAutomationScrollPattern_CachedVerticallyScrollable, uiautomationclient/IUIAutomationScrollPattern::CachedVerticallyScrollable, uiautomationclient/IUIAutomationScrollPattern::get_CachedVerticallyScrollable, winauto.uiauto_IUIAutomationScrollPattern_CachedVerticallyScrollable
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
 - IUIAutomationScrollPattern.CachedVerticallyScrollable
 - IUIAutomationScrollPattern.get_CachedVerticallyScrollable
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uiautomationclient.h
: 
- IUIAutomationScrollPattern.get_CachedVerticallyScrollable
: 
---

# IUIAutomationScrollPattern::get_CachedVerticallyScrollable


## -description


Retrieves a cached value that indicates whether the element can scroll vertically.

This property is read-only.


## -parameters


## -remarks



This property can be dynamic. For example, the content area of the element might not be larger than the current viewable area, meaning that the property is <b>FALSE</b>. However, resizing the element or adding child items can increase the bounds of the content area beyond the viewable area, making the property <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/cb62389c-5a7a-412d-a024-0ce9bc6403a2">IUIAutomationScrollPattern</a>



<a href="https://msdn.microsoft.com/9089e237-2115-47b6-a1eb-eaea5a93586e">IUIAutomationScrollPattern::CachedHorizontallyScrollable</a>
 

 

