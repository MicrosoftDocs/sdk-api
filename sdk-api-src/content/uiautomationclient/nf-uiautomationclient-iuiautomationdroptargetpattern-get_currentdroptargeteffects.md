---
UID: NF:uiautomationclient.IUIAutomationDropTargetPattern.get_CurrentDropTargetEffects
title: IUIAutomationDropTargetPattern::get_CurrentDropTargetEffects (uiautomationclient.h)
description: Retrieves an array of localized strings that enumerate the full set of effects that can happen when the user drops a grabbed element on this drop target as part of a drag-and-drop operation. (IUIAutomationDropTargetPattern.get_CurrentDropTargetEffects)
helpviewer_keywords: ["CurrentDropTargetEffects property [Windows Accessibility]","CurrentDropTargetEffects property [Windows Accessibility]","IUIAutomationDropTargetPattern interface","IUIAutomationDropTargetPattern interface [Windows Accessibility]","CurrentDropTargetEffects property","IUIAutomationDropTargetPattern.CurrentDropTargetEffects","IUIAutomationDropTargetPattern.get_CurrentDropTargetEffects","IUIAutomationDropTargetPattern::CurrentDropTargetEffects","IUIAutomationDropTargetPattern::get_CurrentDropTargetEffects","get_CurrentDropTargetEffects","uiautomationclient/IUIAutomationDropTargetPattern::CurrentDropTargetEffects","uiautomationclient/IUIAutomationDropTargetPattern::get_CurrentDropTargetEffects","winauto.uiauto_iuiautomationdroptargetpattern_currentdroptargeteffects"]
old-location: winauto\uiauto_iuiautomationdroptargetpattern_currentdroptargeteffects.htm
tech.root: WinAuto
ms.assetid: C7AF57B4-E4A0-4105-93C9-38106DCAA077
ms.date: 12/05/2018
ms.keywords: CurrentDropTargetEffects property [Windows Accessibility], CurrentDropTargetEffects property [Windows Accessibility],IUIAutomationDropTargetPattern interface, IUIAutomationDropTargetPattern interface [Windows Accessibility],CurrentDropTargetEffects property, IUIAutomationDropTargetPattern.CurrentDropTargetEffects, IUIAutomationDropTargetPattern.get_CurrentDropTargetEffects, IUIAutomationDropTargetPattern::CurrentDropTargetEffects, IUIAutomationDropTargetPattern::get_CurrentDropTargetEffects, get_CurrentDropTargetEffects, uiautomationclient/IUIAutomationDropTargetPattern::CurrentDropTargetEffects, uiautomationclient/IUIAutomationDropTargetPattern::get_CurrentDropTargetEffects, winauto.uiauto_iuiautomationdroptargetpattern_currentdroptargeteffects
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
 - IUIAutomationDropTargetPattern::get_CurrentDropTargetEffects
 - uiautomationclient/IUIAutomationDropTargetPattern::get_CurrentDropTargetEffects
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
 - IUIAutomationDropTargetPattern.CurrentDropTargetEffects
 - IUIAutomationDropTargetPattern.get_CurrentDropTargetEffects
---

# IUIAutomationDropTargetPattern::get_CurrentDropTargetEffects


## -description

Retrieves an array of localized strings that enumerate the full set of effects that can happen when the user drops a grabbed element on this drop target as part of a drag-and-drop operation.

This property is read-only.

## -parameters

## -remarks

Some drag operations support a set of different drop effects. For example, a drag operation that is initiated with a right-click might display a menu of options for the action that occurs when the element is dropped.  To find out the set of effects that can happen when the grabbed element is dropped, a client can query the DropEffects property of the dragged element.  This property can contain short strings such as "move", or longer ones such as "insert into Main group".  The strings are always localized.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationdroptargetpattern">IUIAutomationDropTargetPattern</a>
