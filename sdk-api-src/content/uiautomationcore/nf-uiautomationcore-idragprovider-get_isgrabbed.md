---
UID: NF:uiautomationcore.IDragProvider.get_IsGrabbed
title: IDragProvider::get_IsGrabbed
author: windows-sdk-content
description: Indicates whether the element has been grabbed as part of a drag-and-drop operation.
old-location: winauto\uiauto_idragprovider_isgrabbed.htm
old-project: WinAuto
ms.assetid: E2A472A0-F9CE-4778-96DD-60B00D53EEA6
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IDragProvider interface [Windows Accessibility],IsGrabbed property, IDragProvider.IsGrabbed, IDragProvider.get_IsGrabbed, IDragProvider::IsGrabbed, IDragProvider::get_IsGrabbed, IsGrabbed property [Windows Accessibility], IsGrabbed property [Windows Accessibility],IDragProvider interface, get_IsGrabbed, uiautomationcore/IDragProvider::IsGrabbed, uiautomationcore/IDragProvider::get_IsGrabbed, winauto.uiauto_idragprovider_isgrabbed
ms.prod: windows
ms.technology: windows-sdk
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
 - IDragProvider.IsGrabbed
 - IDragProvider.get_IsGrabbed
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IDragProvider::get_IsGrabbed


## -description


Indicates whether the element has been grabbed as part of a drag-and-drop operation.

This property is read-only.


## -parameters


## -remarks



If this property changes, the provider must notify clients by calling <a href="https://msdn.microsoft.com/ec9da198-eb1d-4883-9b5c-539c92bd530b">UiaRaiseAutomationPropertyChangedEvent</a> and specifying a property identifier of <a href="https://msdn.microsoft.com/en-us/library/Ee671200(v=VS.85).aspx">UIA_DragIsGrabbedPropertyId</a> or <a href="https://msdn.microsoft.com/en-us/library/Ee671200(v=VS.85).aspx">UIA_DragDropEffectPropertyId</a>.




## -see-also




<a href="https://msdn.microsoft.com/FAC4A56D-17BC-42E6-A03E-EE45D717DE37">IDragProvider</a>
 

 

