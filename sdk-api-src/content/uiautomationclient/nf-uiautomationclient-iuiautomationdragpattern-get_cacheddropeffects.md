---
UID: NF:uiautomationclient.IUIAutomationDragPattern.get_CachedDropEffects
title: IUIAutomationDragPattern::get_CachedDropEffects
author: windows-sdk-content
description: Retrieves a cached array of localized strings that enumerate the full set of effects that can happen when the user drops this element as part of a drag-and-drop operation.
old-location: winauto\uiauto_iuiautomationdragpattern_cacheddropeffects.htm
tech.root: WinAuto
ms.assetid: FDE2A5CA-1353-466E-A28C-E317059AEA54
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: CachedDropEffects property [Windows Accessibility], CachedDropEffects property [Windows Accessibility],IUIAutomationDragPattern interface, IUIAutomationDragPattern interface [Windows Accessibility],CachedDropEffects property, IUIAutomationDragPattern.CachedDropEffects, IUIAutomationDragPattern.get_CachedDropEffects, IUIAutomationDragPattern::CachedDropEffects, IUIAutomationDragPattern::get_CachedDropEffects, get_CachedDropEffects, uiautomationclient/IUIAutomationDragPattern::CachedDropEffects, uiautomationclient/IUIAutomationDragPattern::get_CachedDropEffects, winauto.uiauto_iuiautomationdragpattern_cacheddropeffects
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
 - IUIAutomationDragPattern.CachedDropEffects
 - IUIAutomationDragPattern.get_CachedDropEffects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationDragPattern::get_CachedDropEffects


## -description


Retrieves a cached array of localized strings that enumerate the  full set of effects that can happen when the user drops this element as part of a drag-and-drop operation.

This property is read-only.


## -parameters


## -remarks



Some drag operations support a set of different drop effects. For example, a drag operation that is initiated with a right-click might display a menu of options for the action that occurs when the element is dropped.  In the source-only style of Microsoft UI Automation drag-and-drop, no elements implement the <a href="https://msdn.microsoft.com/DD5EE4A0-E6C0-4657-A60F-7F59FC569E04">DropTarget</a> pattern.  To find out the set of effects that can happen when the grabbed element is dropped, a client can query the <a href="https://msdn.microsoft.com/66DEC1A0-5AB4-41C7-AA7A-F512AE388999">DropEffects</a> property of the dragged element.  This property can contain short strings such as "move", or  longer ones such as "insert into Main group".  The strings are always localized.




## -see-also




<a href="https://msdn.microsoft.com/F7768A87-3981-48E0-A72D-BEA14C189E6E">IUIAutomationDragPattern</a>
 

 

