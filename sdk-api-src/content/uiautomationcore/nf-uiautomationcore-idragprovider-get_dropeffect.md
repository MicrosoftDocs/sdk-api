---
UID: NF:uiautomationcore.IDragProvider.get_DropEffect
title: IDragProvider::get_DropEffect
author: windows-sdk-content
description: Retrieves a localized string that indicates what happens when this element is dropped as part of a drag-drop operation.
old-location: winauto\uiauto_idragprovider_dropeffect.htm
old-project: WinAuto
ms.assetid: 90850574-83EA-4291-99D0-391D8CACFE9F
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DropEffect property [Windows Accessibility], DropEffect property [Windows Accessibility],IDragProvider interface, IDragProvider interface [Windows Accessibility],DropEffect property, IDragProvider.DropEffect, IDragProvider.get_DropEffect, IDragProvider::DropEffect, IDragProvider::get_DropEffect, get_DropEffect, uiautomationcore/IDragProvider::DropEffect, uiautomationcore/IDragProvider::get_DropEffect, winauto.uiauto_idragprovider_dropeffect
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - IDragProvider.DropEffect
 - IDragProvider.get_DropEffect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IDragProvider::get_DropEffect


## -description


Retrieves a localized string that indicates what happens when this element is dropped as part of a drag-drop operation.

This property is read-only.


## -parameters


## -remarks



In the source-only style of UI Automation drag-and-drop, no elements implement the <a href="https://msdn.microsoft.com/DD5EE4A0-E6C0-4657-A60F-7F59FC569E04">DropTarget</a> pattern.  To find out what effect dropping the dragged element will have, a client can query the <b>DropEffect</b> property of the dragged element.  This property can be a short string such as "move", or a longer one, such as "insert into Main group".  The string is always localized.

If this property changes, the provider must notify clients by calling <a href="https://msdn.microsoft.com/ec9da198-eb1d-4883-9b5c-539c92bd530b">UiaRaiseAutomationPropertyChangedEvent</a> and specifying a property identifier of <a href="uiauto_control_pattern_propids.htm">UIA_DragIsGrabbedPropertyId</a> or <a href="uiauto_control_pattern_propids.htm">UIA_DragDropEffectPropertyId</a>.




## -see-also




<a href="https://msdn.microsoft.com/FAC4A56D-17BC-42E6-A03E-EE45D717DE37">IDragProvider</a>
 

 

