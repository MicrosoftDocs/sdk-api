---
UID: NF:uiautomationcore.IDropTargetProvider.get_DropTargetEffects
title: IDropTargetProvider::get_DropTargetEffects
author: windows-sdk-content
description: Retrieves an array of localized strings that enumerate the full set of effects that can happen when the user drops a grabbed element on this drop target as part of a drag-and-drop operation.
old-location: winauto\uiauto_idroptargetprovider_droptargeteffects.htm
tech.root: WinAuto
ms.assetid: FF4080DD-CED0-4F3C-9F0C-BB37BA94DC7D
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: DropTargetEffects property [Windows Accessibility], DropTargetEffects property [Windows Accessibility],IDropTargetProvider interface, IDropTargetProvider interface [Windows Accessibility],DropTargetEffects property, IDropTargetProvider.DropTargetEffects, IDropTargetProvider.get_DropTargetEffects, IDropTargetProvider::DropTargetEffects, IDropTargetProvider::get_DropTargetEffects, get_DropTargetEffects, uiautomationcore/IDropTargetProvider::DropTargetEffects, uiautomationcore/IDropTargetProvider::get_DropTargetEffects, winauto.uiauto_idroptargetprovider_droptargeteffects
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
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
 - UIAutomationCore.h
api_name:
 - IDropTargetProvider.DropTargetEffects
 - IDropTargetProvider.get_DropTargetEffects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDropTargetProvider::get_DropTargetEffects


## -description


Retrieves an array of localized strings that enumerate the full set of effects that can happen when the user drops a grabbed element on this drop target as part of a drag-and-drop operation.

This property is read-only.


## -parameters


## -remarks



Some drag operations support a set of different drop effects. For example, a drag operation that is initiated with a right-click might display a menu of options for the action that occurs when the element is dropped.  To find out the set of effects that can happen when the grabbed element is dropped, a client can query the <a href="https://msdn.microsoft.com/66DEC1A0-5AB4-41C7-AA7A-F512AE388999">DropEffects</a> property of the dragged element.  This property can contain short strings such as "move", or longer ones such as "insert into Main group".  The strings are always localized.




## -see-also




<a href="https://msdn.microsoft.com/ECCDC429-4829-46E0-AE77-270024E2DA48">IDropTargetProvider</a>
 

 

