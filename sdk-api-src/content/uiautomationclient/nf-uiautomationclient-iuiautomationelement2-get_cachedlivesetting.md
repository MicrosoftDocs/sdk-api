---
UID: NF:uiautomationclient.IUIAutomationElement2.get_CachedLiveSetting
title: IUIAutomationElement2::get_CachedLiveSetting (uiautomationclient.h)
description: Retrieves a cached value that indicates the type of notifications, if any, that the element sends when the content of the element changes.
helpviewer_keywords: ["CachedLiveSetting property [Windows Accessibility]","CachedLiveSetting property [Windows Accessibility]","IUIAutomationElement2 interface","IUIAutomationElement2 interface [Windows Accessibility]","CachedLiveSetting property","IUIAutomationElement2.CachedLiveSetting","IUIAutomationElement2.get_CachedLiveSetting","IUIAutomationElement2::CachedLiveSetting","IUIAutomationElement2::get_CachedLiveSetting","get_CachedLiveSetting","uiautomationclient/IUIAutomationElement2::CachedLiveSetting","uiautomationclient/IUIAutomationElement2::get_CachedLiveSetting","winauto.uiauto_iuiautomationelement2_cachedlivesetting"]
old-location: winauto\uiauto_iuiautomationelement2_cachedlivesetting.htm
tech.root: WinAuto
ms.assetid: 5DAE4E4B-A93D-4743-907E-29FC4B6D9101
ms.date: 12/05/2018
ms.keywords: CachedLiveSetting property [Windows Accessibility], CachedLiveSetting property [Windows Accessibility],IUIAutomationElement2 interface, IUIAutomationElement2 interface [Windows Accessibility],CachedLiveSetting property, IUIAutomationElement2.CachedLiveSetting, IUIAutomationElement2.get_CachedLiveSetting, IUIAutomationElement2::CachedLiveSetting, IUIAutomationElement2::get_CachedLiveSetting, get_CachedLiveSetting, uiautomationclient/IUIAutomationElement2::CachedLiveSetting, uiautomationclient/IUIAutomationElement2::get_CachedLiveSetting, winauto.uiauto_iuiautomationelement2_cachedlivesetting
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationElement2::get_CachedLiveSetting
 - uiautomationclient/IUIAutomationElement2::get_CachedLiveSetting
dev_langs:
 - c++
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
---

# IUIAutomationElement2::get_CachedLiveSetting


## -description

Retrieves a cached value that indicates the type of notifications, if any, that the element sends when the content of the element changes. 

This property is read-only.

## -parameters

### -param retVal

## -remarks

This property maps to the Accessible Rich Internet Applications (ARIA)<b> live</b> property.

The LiveSetting property is supported by provider elements that are part of a live region. When the content of a live region changes, the provider element can raise a notification. A client application determines whether to notify the user of the changes based on the value of the LiveSetting property.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement2-get_currentlivesetting">CurrentLiveSetting</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement2">IUIAutomationElement2</a>



<a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-livesetting">LiveSetting</a>