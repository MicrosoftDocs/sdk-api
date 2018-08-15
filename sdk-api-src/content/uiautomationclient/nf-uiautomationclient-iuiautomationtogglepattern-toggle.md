---
UID: NF:uiautomationclient.IUIAutomationTogglePattern.Toggle
title: IUIAutomationTogglePattern::Toggle
author: windows-sdk-content
description: Cycles through the toggle states of the control.
old-location: winauto\uiauto_IUIAutomationTogglePattern_Toggle.htm
old-project: WinAuto
ms.assetid: 5d1e6474-e8fb-47a2-9130-539d1b9f230e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IUIAutomationTogglePattern interface [Windows Accessibility],Toggle method, IUIAutomationTogglePattern.Toggle, IUIAutomationTogglePattern::Toggle, Toggle, Toggle method [Windows Accessibility], Toggle method [Windows Accessibility],IUIAutomationTogglePattern interface, uiauto.uiauto_IUIAutomationTogglePattern_Toggle, uiauto_IUIAutomationTogglePattern_Toggle, uiautomationclient/IUIAutomationTogglePattern::Toggle, winauto.uiauto_IUIAutomationTogglePattern_Toggle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
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
 - IUIAutomationTogglePattern.Toggle
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationTogglePattern::Toggle


## -description


Cycles through the toggle states of the control.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A control cycles through its states in this order: <a href="uiauto_ToggleState.htm">ToggleState_On</a>, <a href="uiauto_ToggleState.htm">ToggleState_Off</a> and, if supported, <a href="uiauto_ToggleState.htm">ToggleState_Indeterminate</a>.



