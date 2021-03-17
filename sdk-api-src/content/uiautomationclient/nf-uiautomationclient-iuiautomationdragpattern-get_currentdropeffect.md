---
UID: NF:uiautomationclient.IUIAutomationDragPattern.get_CurrentDropEffect
title: IUIAutomationDragPattern::get_CurrentDropEffect (uiautomationclient.h)
description: Retrieves a localized string that indicates what happens when the user drops this element as part of a drag-drop operation.
helpviewer_keywords: ["CurrentDropEffect property [Windows Accessibility]","CurrentDropEffect property [Windows Accessibility]","IUIAutomationDragPattern interface","IUIAutomationDragPattern interface [Windows Accessibility]","CurrentDropEffect property","IUIAutomationDragPattern.CurrentDropEffect","IUIAutomationDragPattern.get_CurrentDropEffect","IUIAutomationDragPattern::CurrentDropEffect","IUIAutomationDragPattern::get_CurrentDropEffect","get_CurrentDropEffect","uiautomationclient/IUIAutomationDragPattern::CurrentDropEffect","uiautomationclient/IUIAutomationDragPattern::get_CurrentDropEffect","winauto.uiauto_iuiautomationdragpattern_currentdropeffect"]
old-location: winauto\uiauto_iuiautomationdragpattern_currentdropeffect.htm
tech.root: WinAuto
ms.assetid: 8F5459DE-4BAA-412D-88E9-A81125150CAA
ms.date: 12/05/2018
ms.keywords: CurrentDropEffect property [Windows Accessibility], CurrentDropEffect property [Windows Accessibility],IUIAutomationDragPattern interface, IUIAutomationDragPattern interface [Windows Accessibility],CurrentDropEffect property, IUIAutomationDragPattern.CurrentDropEffect, IUIAutomationDragPattern.get_CurrentDropEffect, IUIAutomationDragPattern::CurrentDropEffect, IUIAutomationDragPattern::get_CurrentDropEffect, get_CurrentDropEffect, uiautomationclient/IUIAutomationDragPattern::CurrentDropEffect, uiautomationclient/IUIAutomationDragPattern::get_CurrentDropEffect, winauto.uiauto_iuiautomationdragpattern_currentdropeffect
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
 - IUIAutomationDragPattern::get_CurrentDropEffect
 - uiautomationclient/IUIAutomationDragPattern::get_CurrentDropEffect
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
 - IUIAutomationDragPattern.CurrentDropEffect
 - IUIAutomationDragPattern.get_CurrentDropEffect
---

# IUIAutomationDragPattern::get_CurrentDropEffect


## -description

Retrieves a localized string that indicates what happens when the user drops this element as part of a drag-drop operation.  

This property is read-only.

## -parameters

## -remarks

In the source-only style of Microsoft UI Automation drag-and-drop, no elements implement the <a href="/windows/desktop/WinAuto/uiauto-implementingdroptarget">DropTarget</a> pattern.  To find out what effect dropping the dragged element will have, a client can query the <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-idragprovider-get_dropeffect">DropEffect</a> property of the dragged element.  This property can be a short string such as "move", or a longer one, such as "insert into Main group".  The string is always localized.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationdragpattern">IUIAutomationDragPattern</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationdroptargetpattern-get_cacheddroptargeteffect">IUIAutomationDropTargetPattern::CachedDropTargetEffect</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationdroptargetpattern-get_currentdroptargeteffect">IUIAutomationDropTargetPattern::CurrentDropTargetEffect</a>



<a href="/windows/desktop/WinAuto/ui-automation-support-for-drag-and-drop">UI Automation Support for Drag-and-Drop</a>