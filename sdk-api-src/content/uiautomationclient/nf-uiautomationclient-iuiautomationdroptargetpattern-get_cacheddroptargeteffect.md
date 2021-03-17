---
UID: NF:uiautomationclient.IUIAutomationDropTargetPattern.get_CachedDropTargetEffect
title: IUIAutomationDropTargetPattern::get_CachedDropTargetEffect (uiautomationclient.h)
description: Retrieves a cached localized string that describes what happens when the user drops the grabbed element on this drop target.
helpviewer_keywords: ["CachedDropTargetEffect property [Windows Accessibility]","CachedDropTargetEffect property [Windows Accessibility]","IUIAutomationDropTargetPattern interface","IUIAutomationDropTargetPattern interface [Windows Accessibility]","CachedDropTargetEffect property","IUIAutomationDropTargetPattern.CachedDropTargetEffect","IUIAutomationDropTargetPattern.get_CachedDropTargetEffect","IUIAutomationDropTargetPattern::CachedDropTargetEffect","IUIAutomationDropTargetPattern::get_CachedDropTargetEffect","get_CachedDropTargetEffect","uiautomationclient/IUIAutomationDropTargetPattern::CachedDropTargetEffect","uiautomationclient/IUIAutomationDropTargetPattern::get_CachedDropTargetEffect","winauto.uiauto_iuiautomationdroptargetpattern_cacheddroptargeteffect"]
old-location: winauto\uiauto_iuiautomationdroptargetpattern_cacheddroptargeteffect.htm
tech.root: WinAuto
ms.assetid: 083B9B3C-B4B8-4336-8614-61899FBC5E47
ms.date: 12/05/2018
ms.keywords: CachedDropTargetEffect property [Windows Accessibility], CachedDropTargetEffect property [Windows Accessibility],IUIAutomationDropTargetPattern interface, IUIAutomationDropTargetPattern interface [Windows Accessibility],CachedDropTargetEffect property, IUIAutomationDropTargetPattern.CachedDropTargetEffect, IUIAutomationDropTargetPattern.get_CachedDropTargetEffect, IUIAutomationDropTargetPattern::CachedDropTargetEffect, IUIAutomationDropTargetPattern::get_CachedDropTargetEffect, get_CachedDropTargetEffect, uiautomationclient/IUIAutomationDropTargetPattern::CachedDropTargetEffect, uiautomationclient/IUIAutomationDropTargetPattern::get_CachedDropTargetEffect, winauto.uiauto_iuiautomationdroptargetpattern_cacheddroptargeteffect
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
 - IUIAutomationDropTargetPattern::get_CachedDropTargetEffect
 - uiautomationclient/IUIAutomationDropTargetPattern::get_CachedDropTargetEffect
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
 - IUIAutomationDropTargetPattern.CachedDropTargetEffect
 - IUIAutomationDropTargetPattern.get_CachedDropTargetEffect
---

# IUIAutomationDropTargetPattern::get_CachedDropTargetEffect


## -description

Retrieves a cached localized string that describes what happens when the user drops the grabbed element on this drop target.

This property is read-only.

## -parameters

## -remarks

This property describes the default effect that happens when the user drops a grabbed element on a target, such as moving or copying the element.  This property can be a short string such as "move", or a longer one such as "insert into Main group".  The string is always localized.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationdroptargetpattern">IUIAutomationDropTargetPattern</a>