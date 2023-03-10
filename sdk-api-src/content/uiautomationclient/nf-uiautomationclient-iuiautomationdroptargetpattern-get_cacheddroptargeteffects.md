---
UID: NF:uiautomationclient.IUIAutomationDropTargetPattern.get_CachedDropTargetEffects
title: IUIAutomationDropTargetPattern::get_CachedDropTargetEffects (uiautomationclient.h)
description: Retrieves a cached array of localized strings that enumerate the full set of effects that can happen when the user drops a grabbed element on this drop target as part of a drag-and-drop operation.
helpviewer_keywords: ["CachedDropTargetEffects property [Windows Accessibility]","CachedDropTargetEffects property [Windows Accessibility]","IUIAutomationDropTargetPattern interface","IUIAutomationDropTargetPattern interface [Windows Accessibility]","CachedDropTargetEffects property","IUIAutomationDropTargetPattern.CachedDropTargetEffects","IUIAutomationDropTargetPattern.get_CachedDropTargetEffects","IUIAutomationDropTargetPattern::CachedDropTargetEffects","IUIAutomationDropTargetPattern::get_CachedDropTargetEffects","get_CachedDropTargetEffects","uiautomationclient/IUIAutomationDropTargetPattern::CachedDropTargetEffects","uiautomationclient/IUIAutomationDropTargetPattern::get_CachedDropTargetEffects","winauto.uiauto_iuiautomationdroptargetpattern_cacheddroptargeteffects"]
old-location: winauto\uiauto_iuiautomationdroptargetpattern_cacheddroptargeteffects.htm
tech.root: WinAuto
ms.assetid: 6F61F13B-0E5B-449D-A237-FF494B730392
ms.date: 12/05/2018
ms.keywords: CachedDropTargetEffects property [Windows Accessibility], CachedDropTargetEffects property [Windows Accessibility],IUIAutomationDropTargetPattern interface, IUIAutomationDropTargetPattern interface [Windows Accessibility],CachedDropTargetEffects property, IUIAutomationDropTargetPattern.CachedDropTargetEffects, IUIAutomationDropTargetPattern.get_CachedDropTargetEffects, IUIAutomationDropTargetPattern::CachedDropTargetEffects, IUIAutomationDropTargetPattern::get_CachedDropTargetEffects, get_CachedDropTargetEffects, uiautomationclient/IUIAutomationDropTargetPattern::CachedDropTargetEffects, uiautomationclient/IUIAutomationDropTargetPattern::get_CachedDropTargetEffects, winauto.uiauto_iuiautomationdroptargetpattern_cacheddroptargeteffects
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
 - IUIAutomationDropTargetPattern::get_CachedDropTargetEffects
 - uiautomationclient/IUIAutomationDropTargetPattern::get_CachedDropTargetEffects
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
 - IUIAutomationDropTargetPattern.CachedDropTargetEffects
 - IUIAutomationDropTargetPattern.get_CachedDropTargetEffects
---

# IUIAutomationDropTargetPattern::get_CachedDropTargetEffects


## -description

Retrieves a cached array of localized strings that enumerate the full set of effects that can happen when the user drops a grabbed element on this drop target as part of a drag-and-drop operation.

This property is read-only.

## -parameters

## -remarks

Some drag operations support a set of different drop effects. For example, a drag operation that is initiated with a right-click might display a menu of options for the action that occurs when the element is dropped.  To find out the set of effects that can happen when the grabbed element is dropped, a client can query the DropEffects property of the dragged element.  This property can contain short strings such as "move", or longer ones such as "insert into Main group".  The strings are always localized.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationdroptargetpattern">IUIAutomationDropTargetPattern</a>