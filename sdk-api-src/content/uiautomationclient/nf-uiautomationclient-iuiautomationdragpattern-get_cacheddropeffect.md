---
UID: NF:uiautomationclient.IUIAutomationDragPattern.get_CachedDropEffect
title: IUIAutomationDragPattern::get_CachedDropEffect (uiautomationclient.h)
description: Retrieves a cached localized string that indicates what happens when the user drops this element as part of a drag-and-drop operation.
helpviewer_keywords: ["CachedDropEffect property [Windows Accessibility]","CachedDropEffect property [Windows Accessibility]","IUIAutomationDragPattern interface","IUIAutomationDragPattern interface [Windows Accessibility]","CachedDropEffect property","IUIAutomationDragPattern.CachedDropEffect","IUIAutomationDragPattern.get_CachedDropEffect","IUIAutomationDragPattern::CachedDropEffect","IUIAutomationDragPattern::get_CachedDropEffect","get_CachedDropEffect","uiautomationclient/IUIAutomationDragPattern::CachedDropEffect","uiautomationclient/IUIAutomationDragPattern::get_CachedDropEffect","winauto.uiauto_iuiautomationdragpattern_cacheddropeffect"]
old-location: winauto\uiauto_iuiautomationdragpattern_cacheddropeffect.htm
tech.root: WinAuto
ms.assetid: A99F5E0F-FC61-4AD7-9DC8-B4B7B1AB2F6C
ms.date: 12/05/2018
ms.keywords: CachedDropEffect property [Windows Accessibility], CachedDropEffect property [Windows Accessibility],IUIAutomationDragPattern interface, IUIAutomationDragPattern interface [Windows Accessibility],CachedDropEffect property, IUIAutomationDragPattern.CachedDropEffect, IUIAutomationDragPattern.get_CachedDropEffect, IUIAutomationDragPattern::CachedDropEffect, IUIAutomationDragPattern::get_CachedDropEffect, get_CachedDropEffect, uiautomationclient/IUIAutomationDragPattern::CachedDropEffect, uiautomationclient/IUIAutomationDragPattern::get_CachedDropEffect, winauto.uiauto_iuiautomationdragpattern_cacheddropeffect
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
 - IUIAutomationDragPattern::get_CachedDropEffect
 - uiautomationclient/IUIAutomationDragPattern::get_CachedDropEffect
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
 - IUIAutomationDragPattern.CachedDropEffect
 - IUIAutomationDragPattern.get_CachedDropEffect
---

# IUIAutomationDragPattern::get_CachedDropEffect


## -description

Retrieves a cached localized string that indicates what happens when the user drops this element as part of a drag-and-drop operation.  

This property is read-only.

## -parameters

## -remarks

In the source-only style of Microsoft UI Automation drag-and-drop, no elements implement the <a href="/windows/desktop/WinAuto/uiauto-implementingdroptarget">DropTarget</a> pattern.  To find out what effect dropping the dragged element will have, a client can query the <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-idragprovider-get_dropeffect">DropEffect</a> property of the dragged element.  This property can be a short string such as "move", or a longer one, such as "insert into Main group".  The string is always localized.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationdragpattern">IUIAutomationDragPattern</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationdroptargetpattern-get_cacheddroptargeteffect">IUIAutomationDropTargetPattern::CachedDropTargetEffect</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationdroptargetpattern-get_currentdroptargeteffect">IUIAutomationDropTargetPattern::CurrentDropTargetEffect</a>



<a href="/windows/desktop/WinAuto/ui-automation-support-for-drag-and-drop">UI Automation Support for Drag-and-Drop</a>