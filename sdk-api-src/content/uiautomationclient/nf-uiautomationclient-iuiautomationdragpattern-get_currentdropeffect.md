---
UID: NF:uiautomationclient.IUIAutomationDragPattern.get_CurrentDropEffect
title: IUIAutomationDragPattern::get_CurrentDropEffect
author: windows-sdk-content
description: Retrieves a localized string that indicates what happens when the user drops this element as part of a drag-drop operation.
old-location: winauto\uiauto_iuiautomationdragpattern_currentdropeffect.htm
tech.root: WinAuto
ms.assetid: 8F5459DE-4BAA-412D-88E9-A81125150CAA
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CurrentDropEffect property [Windows Accessibility], CurrentDropEffect property [Windows Accessibility],IUIAutomationDragPattern interface, IUIAutomationDragPattern interface [Windows Accessibility],CurrentDropEffect property, IUIAutomationDragPattern.CurrentDropEffect, IUIAutomationDragPattern.get_CurrentDropEffect, IUIAutomationDragPattern::CurrentDropEffect, IUIAutomationDragPattern::get_CurrentDropEffect, get_CurrentDropEffect, uiautomationclient/IUIAutomationDragPattern::CurrentDropEffect, uiautomationclient/IUIAutomationDragPattern::get_CurrentDropEffect, winauto.uiauto_iuiautomationdragpattern_currentdropeffect
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
 - IUIAutomationDragPattern.CurrentDropEffect
 - IUIAutomationDragPattern.get_CurrentDropEffect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uiautomationclient.h
: 
- IUIAutomationDragPattern.get_CurrentDropEffect
: 
---

# IUIAutomationDragPattern::get_CurrentDropEffect


## -description


Retrieves a localized string that indicates what happens when the user drops this element as part of a drag-drop operation.  

This property is read-only.


## -parameters


## -remarks



In the source-only style of Microsoft UI Automation drag-and-drop, no elements implement the <a href="https://msdn.microsoft.com/DD5EE4A0-E6C0-4657-A60F-7F59FC569E04">DropTarget</a> pattern.  To find out what effect dropping the dragged element will have, a client can query the <a href="https://msdn.microsoft.com/90850574-83EA-4291-99D0-391D8CACFE9F">DropEffect</a> property of the dragged element.  This property can be a short string such as "move", or a longer one, such as "insert into Main group".  The string is always localized.




## -see-also




<a href="https://msdn.microsoft.com/F7768A87-3981-48E0-A72D-BEA14C189E6E">IUIAutomationDragPattern</a>



<a href="https://msdn.microsoft.com/083B9B3C-B4B8-4336-8614-61899FBC5E47">IUIAutomationDropTargetPattern::CachedDropTargetEffect</a>



<a href="https://msdn.microsoft.com/C7A2C62B-D61B-4884-BEF0-E4EB1088D1AB">IUIAutomationDropTargetPattern::CurrentDropTargetEffect</a>



<a href="https://msdn.microsoft.com/FFF5A296-C9FF-4B47-AAF8-A9DD581D9DBE">UI Automation Support for Drag-and-Drop</a>
 

 

