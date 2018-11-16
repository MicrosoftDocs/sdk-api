---
UID: NF:uiautomationcore.IToggleProvider.Toggle
title: IToggleProvider::Toggle
author: windows-sdk-content
description: Cycles through the toggle states of a control.
old-location: winauto\uiauto_IToggleProvider_Toggle.htm
tech.root: WinAuto
ms.assetid: afadbcaf-156f-496e-a0f3-900e7f8d44da
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IToggleProvider interface [Windows Accessibility],Toggle method, IToggleProvider.Toggle, IToggleProvider::Toggle, Toggle, Toggle method [Windows Accessibility], Toggle method [Windows Accessibility],IToggleProvider interface, uiauto.uiauto_IToggleProvider_Toggle, uiauto_IToggleProvider_Toggle, uiautomationcore/IToggleProvider::Toggle, winauto.uiauto_IToggleProvider_Toggle
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
 - IToggleProvider.Toggle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uiautomationcore.h
: 
- IToggleProvider.Toggle
: 
---

# IToggleProvider::Toggle


## -description


Cycles through the toggle states of a control.
        


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A control must cycle through its <a href="https://msdn.microsoft.com/242031d6-2d55-478d-b029-5a3b0a251601">ToggleState</a> in this order: 
<b>ToggleState_On</b>, <b>ToggleState_Off</b> 
and, if supported, <b>ToggleState_Indeterminate</b>.
		




## -see-also




<a href="https://msdn.microsoft.com/85da8225-31b8-4b4d-81f4-ad98871b8e31">IToggleProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

