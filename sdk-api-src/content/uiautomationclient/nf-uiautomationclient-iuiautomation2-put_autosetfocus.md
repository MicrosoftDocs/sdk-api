---
UID: NF:uiautomationclient.IUIAutomation2.put_AutoSetFocus
title: IUIAutomation2::put_AutoSetFocus (uiautomationclient.h)
description: Specifies whether calls to UI Automation control pattern methods automatically set focus to the target element. (Put)
helpviewer_keywords: ["AutoSetFocus property [Windows Accessibility]","AutoSetFocus property [Windows Accessibility]","IUIAutomation2 interface","IUIAutomation2 interface [Windows Accessibility]","AutoSetFocus property","IUIAutomation2.AutoSetFocus","IUIAutomation2.put_AutoSetFocus","IUIAutomation2::AutoSetFocus","IUIAutomation2::get_AutoSetFocus","IUIAutomation2::put_AutoSetFocus","put_AutoSetFocus","uiautomationclient/IUIAutomation2::AutoSetFocus","uiautomationclient/IUIAutomation2::get_AutoSetFocus","uiautomationclient/IUIAutomation2::put_AutoSetFocus","winauto.uiauto_IUIAutomation2_AutoSetFocus"]
old-location: winauto\uiauto_IUIAutomation2_AutoSetFocus.htm
tech.root: WinAuto
ms.assetid: 86B0C641-6A5B-4E1A-ADB8-7663B246739B
ms.date: 12/05/2018
ms.keywords: AutoSetFocus property [Windows Accessibility], AutoSetFocus property [Windows Accessibility],IUIAutomation2 interface, IUIAutomation2 interface [Windows Accessibility],AutoSetFocus property, IUIAutomation2.AutoSetFocus, IUIAutomation2.put_AutoSetFocus, IUIAutomation2::AutoSetFocus, IUIAutomation2::get_AutoSetFocus, IUIAutomation2::put_AutoSetFocus, put_AutoSetFocus, uiautomationclient/IUIAutomation2::AutoSetFocus, uiautomationclient/IUIAutomation2::get_AutoSetFocus, uiautomationclient/IUIAutomation2::put_AutoSetFocus, winauto.uiauto_IUIAutomation2_AutoSetFocus
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
req.dll: UIAutomationCore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomation2::put_AutoSetFocus
 - uiautomationclient/IUIAutomation2::put_AutoSetFocus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IUIAutomation2.AutoSetFocus
 - IUIAutomation2.get_AutoSetFocus
 - IUIAutomation2.put_AutoSetFocus
---

# IUIAutomation2::put_AutoSetFocus


## -description

Specifies whether calls to UI Automation control pattern methods automatically set focus to the target element.

This property is read/write.

## -parameters

## -remarks

 By default, most UI Automation methods that perform an action on an element, such as <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationinvokepattern-invoke">IUIAutomationInvokePattern::Invoke</a> and <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationvaluepattern-setvalue">IUIAutomationValuePattern::SetValue</a>, set focus to the element before performing the action. For most applications, setting the focus results in a more consistent user experience.  In situations where setting the focus would be disruptive, such as automating a drop-down menu, you can set <b>AutoSetFocus</b> to FALSE to prevent UI Automation methods from setting the focus.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation2">IUIAutomation2</a>
