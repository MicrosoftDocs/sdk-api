---
UID: NF:uiautomationcore.IToggleProvider.get_ToggleState
title: IToggleProvider::get_ToggleState
author: windows-sdk-content
description: Specifies the toggle state of the control.
old-location: winauto\uiauto_IToggleProvider_ToggleState.htm
tech.root: WinAuto
ms.assetid: 57bd9b77-32f4-4abf-b942-c0fe00398e56
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IToggleProvider interface [Windows Accessibility],ToggleState property, IToggleProvider.ToggleState, IToggleProvider.get_ToggleState, IToggleProvider::ToggleState, IToggleProvider::get_ToggleState, ToggleState property [Windows Accessibility], ToggleState property [Windows Accessibility],IToggleProvider interface, get_ToggleState, uiauto.uiauto_IToggleProvider_ToggleState, uiauto_IToggleProvider_ToggleState, uiautomationcore/IToggleProvider::ToggleState, uiautomationcore/IToggleProvider::get_ToggleState, winauto.uiauto_IToggleProvider_ToggleState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - IToggleProvider.ToggleState
 - IToggleProvider.get_ToggleState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IToggleProvider::get_ToggleState


## -description


Specifies the toggle state of the control.

This property is read-only.


## -parameters


## -remarks



A control must cycle through its <a href="https://msdn.microsoft.com/242031d6-2d55-478d-b029-5a3b0a251601">ToggleState</a> in this order:  
<b>ToggleState_On</b>, <b>ToggleState_Off</b> 
and, if supported, <b>ToggleState_Indeterminate</b>.

		




## -see-also




<a href="https://msdn.microsoft.com/85da8225-31b8-4b4d-81f4-ad98871b8e31">IToggleProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

