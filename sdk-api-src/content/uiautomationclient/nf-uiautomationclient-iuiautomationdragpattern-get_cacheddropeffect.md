---
UID: NF:uiautomationclient.IUIAutomationDragPattern.get_CachedDropEffect
title: IUIAutomationDragPattern::get_CachedDropEffect
author: windows-sdk-content
description: Retrieves a cached localized string that indicates what happens when the user drops this element as part of a drag-and-drop operation.
old-location: winauto\uiauto_iuiautomationdragpattern_cacheddropeffect.htm
old-project: WinAuto
ms.assetid: A99F5E0F-FC61-4AD7-9DC8-B4B7B1AB2F6C
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: CachedDropEffect property [Windows Accessibility], CachedDropEffect property [Windows Accessibility],IUIAutomationDragPattern interface, IUIAutomationDragPattern interface [Windows Accessibility],CachedDropEffect property, IUIAutomationDragPattern.CachedDropEffect, IUIAutomationDragPattern.get_CachedDropEffect, IUIAutomationDragPattern::CachedDropEffect, IUIAutomationDragPattern::get_CachedDropEffect, get_CachedDropEffect, uiautomationclient/IUIAutomationDragPattern::CachedDropEffect, uiautomationclient/IUIAutomationDragPattern::get_CachedDropEffect, winauto.uiauto_iuiautomationdragpattern_cacheddropeffect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.redist: 
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
tech.root: 
req.typenames: 
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationDragPattern::get_CachedDropEffect


## -description


Retrieves a cached localized string that indicates what happens when the user drops this element as part of a drag-and-drop operation.  

This property is read-only.


## -parameters


## -remarks



In the source-only style of Microsoft UI Automation drag-and-drop, no elements implement the <a href="https://msdn.microsoft.com/DD5EE4A0-E6C0-4657-A60F-7F59FC569E04">DropTarget</a> pattern.  To find out what effect dropping the dragged element will have, a client can query the <a href="https://msdn.microsoft.com/90850574-83EA-4291-99D0-391D8CACFE9F">DropEffect</a> property of the dragged element.  This property can be a short string such as "move", or a longer one, such as "insert into Main group".  The string is always localized.




## -see-also




<a href="https://msdn.microsoft.com/F7768A87-3981-48E0-A72D-BEA14C189E6E">IUIAutomationDragPattern</a>



<a href="https://msdn.microsoft.com/083B9B3C-B4B8-4336-8614-61899FBC5E47">IUIAutomationDropTargetPattern::CachedDropTargetEffect</a>



<a href="https://msdn.microsoft.com/C7A2C62B-D61B-4884-BEF0-E4EB1088D1AB">IUIAutomationDropTargetPattern::CurrentDropTargetEffect</a>



<a href="https://msdn.microsoft.com/FFF5A296-C9FF-4B47-AAF8-A9DD581D9DBE">UI Automation Support for Drag-and-Drop</a>
 

 

