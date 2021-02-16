---
UID: NF:uiautomationclient.IUIAutomationDragPattern.get_CurrentDropEffects
title: IUIAutomationDragPattern::get_CurrentDropEffects (uiautomationclient.h)
description: Retrieves an array of localized strings that enumerate the full set of effects that can happen when this element as part of a drag-and-drop operation.
helpviewer_keywords: ["CurrentDropEffects property [Windows Accessibility]","CurrentDropEffects property [Windows Accessibility]","IUIAutomationDragPattern interface","IUIAutomationDragPattern interface [Windows Accessibility]","CurrentDropEffects property","IUIAutomationDragPattern.CurrentDropEffects","IUIAutomationDragPattern.get_CurrentDropEffects","IUIAutomationDragPattern::CurrentDropEffects","IUIAutomationDragPattern::get_CurrentDropEffects","get_CurrentDropEffects","uiautomationclient/IUIAutomationDragPattern::CurrentDropEffects","uiautomationclient/IUIAutomationDragPattern::get_CurrentDropEffects","winauto.uiauto_iuiautomationdragpattern_currentdropeffects"]
old-location: winauto\uiauto_iuiautomationdragpattern_currentdropeffects.htm
tech.root: WinAuto
ms.assetid: 393692C9-AA4E-4C50-8006-39457EB57153
ms.date: 12/05/2018
ms.keywords: CurrentDropEffects property [Windows Accessibility], CurrentDropEffects property [Windows Accessibility],IUIAutomationDragPattern interface, IUIAutomationDragPattern interface [Windows Accessibility],CurrentDropEffects property, IUIAutomationDragPattern.CurrentDropEffects, IUIAutomationDragPattern.get_CurrentDropEffects, IUIAutomationDragPattern::CurrentDropEffects, IUIAutomationDragPattern::get_CurrentDropEffects, get_CurrentDropEffects, uiautomationclient/IUIAutomationDragPattern::CurrentDropEffects, uiautomationclient/IUIAutomationDragPattern::get_CurrentDropEffects, winauto.uiauto_iuiautomationdragpattern_currentdropeffects
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
 - IUIAutomationDragPattern::get_CurrentDropEffects
 - uiautomationclient/IUIAutomationDragPattern::get_CurrentDropEffects
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
 - IUIAutomationDragPattern.CurrentDropEffects
 - IUIAutomationDragPattern.get_CurrentDropEffects
---

# IUIAutomationDragPattern::get_CurrentDropEffects


## -description

Retrieves an array of localized strings that enumerate the  full set of effects that can happen when this element  as part of a drag-and-drop operation.

This property is read-only.

## -parameters

## -remarks

Some drag operations support a set of different drop effects. For example, a drag operation that is initiated with a right-click might display a menu of options for the action that occurs when the element is dropped.  In the source-only style of Microsoft UI Automation drag-and-drop, no elements implement the <a href="/windows/desktop/WinAuto/uiauto-implementingdroptarget">DropTarget</a> pattern.  To find out the set of effects that can happen when the grabbed element is dropped, a client can query the DropEffects property of the dragged element.  This property can contain short strings such as "move", or longer ones such as "insert into Main group".  The strings are always localized.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationdragpattern">IUIAutomationDragPattern</a>