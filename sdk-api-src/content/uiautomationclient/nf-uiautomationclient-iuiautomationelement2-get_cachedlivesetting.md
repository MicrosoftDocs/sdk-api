---
UID: NF:uiautomationclient.IUIAutomationElement2.get_CachedLiveSetting
title: IUIAutomationElement2::get_CachedLiveSetting
author: windows-sdk-content
description: Retrieves a cached value that indicates the type of notifications, if any, that the element sends when the content of the element changes.
old-location: winauto\uiauto_iuiautomationelement2_cachedlivesetting.htm
tech.root: WinAuto
ms.assetid: 5DAE4E4B-A93D-4743-907E-29FC4B6D9101
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CachedLiveSetting property [Windows Accessibility], CachedLiveSetting property [Windows Accessibility],IUIAutomationElement2 interface, IUIAutomationElement2 interface [Windows Accessibility],CachedLiveSetting property, IUIAutomationElement2.CachedLiveSetting, IUIAutomationElement2.get_CachedLiveSetting, IUIAutomationElement2::CachedLiveSetting, IUIAutomationElement2::get_CachedLiveSetting, get_CachedLiveSetting, uiautomationclient/IUIAutomationElement2::CachedLiveSetting, uiautomationclient/IUIAutomationElement2::get_CachedLiveSetting, winauto.uiauto_iuiautomationelement2_cachedlivesetting
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IUIAutomationElement2.CachedLiveSetting
 - IUIAutomationElement2.get_CachedLiveSetting
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationElement2::get_CachedLiveSetting


## -description


Retrieves a cached value that indicates the type of notifications, if any, that the element sends when the content of the element changes. 

This property is read-only.


## -parameters


## -remarks



This property maps to the Accessible Rich Internet Applications (ARIA)<b> live</b> property.

The LiveSetting property is supported by provider elements that are part of a live region. When the content of a live region changes, the provider element can raise a notification. A client application determines whether to notify the user of the changes based on the value of the LiveSetting property.




## -see-also




<a href="https://msdn.microsoft.com/3510E0AD-FB79-4636-B6EF-AE0FB62AD55C">CurrentLiveSetting</a>



<a href="https://msdn.microsoft.com/4D9A4E94-BAE9-4E85-8F21-7CABFBE64C6D">IUIAutomationElement2</a>



<a href="https://msdn.microsoft.com/40DD1F00-A9BC-4C84-B2A3-940E37EE9C19">LiveSetting</a>
 

 

