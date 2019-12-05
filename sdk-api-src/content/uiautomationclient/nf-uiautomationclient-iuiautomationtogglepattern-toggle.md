---
UID: NF:uiautomationclient.IUIAutomationTogglePattern.Toggle
title: IUIAutomationTogglePattern::Toggle (uiautomationclient.h)
description: Cycles through the toggle states of the control.
old-location: winauto\uiauto_IUIAutomationTogglePattern_Toggle.htm
tech.root: WinAuto
ms.assetid: 5d1e6474-e8fb-47a2-9130-539d1b9f230e
ms.date: 12/05/2018
ms.keywords: IUIAutomationTogglePattern interface [Windows Accessibility],Toggle method, IUIAutomationTogglePattern.Toggle, IUIAutomationTogglePattern::Toggle, Toggle, Toggle method [Windows Accessibility], Toggle method [Windows Accessibility],IUIAutomationTogglePattern interface, uiauto.uiauto_IUIAutomationTogglePattern_Toggle, uiauto_IUIAutomationTogglePattern_Toggle, uiautomationclient/IUIAutomationTogglePattern::Toggle, winauto.uiauto_IUIAutomationTogglePattern_Toggle
ms.topic: method
f1_keywords:
- uiautomationclient/IUIAutomationTogglePattern.Toggle
dev_langs:
- c++
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
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
- IUIAutomationTogglePattern.Toggle
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationTogglePattern::Toggle


## -description


Cycles through the toggle states of the control.


## -parameters






## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A control cycles through its states in this order: <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/ne-uiautomationcore-togglestate">ToggleState_On</a>, <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/ne-uiautomationcore-togglestate">ToggleState_Off</a> and, if supported, <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/ne-uiautomationcore-togglestate">ToggleState_Indeterminate</a>.



