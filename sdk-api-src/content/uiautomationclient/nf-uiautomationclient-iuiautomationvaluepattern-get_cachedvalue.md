---
UID: NF:uiautomationclient.IUIAutomationValuePattern.get_CachedValue
title: IUIAutomationValuePattern::get_CachedValue
author: windows-sdk-content
description: Retrieves the cached value of the element.
old-location: winauto\uiauto_IUIAutomationValuePattern_CachedValue.htm
old-project: WinAuto
ms.assetid: 32b889d8-952e-4167-9c99-71abc1820c8d
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: CachedValue property [Windows Accessibility], CachedValue property [Windows Accessibility],IUIAutomationValuePattern interface, IUIAutomationValuePattern interface [Windows Accessibility],CachedValue property, IUIAutomationValuePattern.CachedValue, IUIAutomationValuePattern.get_CachedValue, IUIAutomationValuePattern::CachedValue, IUIAutomationValuePattern::get_CachedValue, get_CachedValue, uiauto.uiauto_IUIAutomationValuePattern_CachedValue, uiauto_IUIAutomationValuePattern_CachedValue, uiautomationclient/IUIAutomationValuePattern::CachedValue, uiautomationclient/IUIAutomationValuePattern::get_CachedValue, winauto.uiauto_IUIAutomationValuePattern_CachedValue
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
 - IUIAutomationValuePattern.CachedValue
 - IUIAutomationValuePattern.get_CachedValue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationValuePattern::get_CachedValue


## -description


Retrieves the cached value of the element.

This property is read-only.


## -parameters


## -remarks



Single-line edit controls support programmatic access to their contents through <a href="https://msdn.microsoft.com/07277405-1172-42e5-af51-8e2c1ea06894">IUIAutomationValuePattern</a>. However, multiline edit controls do not support this control pattern, and their contents must be retrieved by using <a href="https://msdn.microsoft.com/ddcf7ecd-7ed2-4b57-82a7-c7e1608dbfa1">IUIAutomationTextPattern</a>.

This property does not support the retrieval of formatting information or substring values. <a href="https://msdn.microsoft.com/ddcf7ecd-7ed2-4b57-82a7-c7e1608dbfa1">IUIAutomationTextPattern</a> must be used in these scenarios as well.




## -see-also




<a href="https://msdn.microsoft.com/07277405-1172-42e5-af51-8e2c1ea06894">IUIAutomationValuePattern</a>
 

 

