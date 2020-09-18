---
UID: NF:uiautomationclient.IUIAutomationElement.get_CurrentControlType
title: IUIAutomationElement::get_CurrentControlType (uiautomationclient.h)
description: Retrieves the control type of the element.
helpviewer_keywords: ["CurrentControlType property [Windows Accessibility]","CurrentControlType property [Windows Accessibility]","IUIAutomationElement interface","IUIAutomationElement interface [Windows Accessibility]","CurrentControlType property","IUIAutomationElement.CurrentControlType","IUIAutomationElement.get_CurrentControlType","IUIAutomationElement::CurrentControlType","IUIAutomationElement::get_CurrentControlType","get_CurrentControlType","uiauto.uiauto_IUIAutomationElement_CurrentControlType","uiauto_IUIAutomationElement_CurrentControlType","uiautomationclient/IUIAutomationElement::CurrentControlType","uiautomationclient/IUIAutomationElement::get_CurrentControlType","winauto.uiauto_IUIAutomationElement_CurrentControlType"]
old-location: winauto\uiauto_IUIAutomationElement_CurrentControlType.htm
tech.root: WinAuto
ms.assetid: 6bceeabd-be77-4820-842a-d343fa2857bd
ms.date: 12/05/2018
ms.keywords: CurrentControlType property [Windows Accessibility], CurrentControlType property [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],CurrentControlType property, IUIAutomationElement.CurrentControlType, IUIAutomationElement.get_CurrentControlType, IUIAutomationElement::CurrentControlType, IUIAutomationElement::get_CurrentControlType, get_CurrentControlType, uiauto.uiauto_IUIAutomationElement_CurrentControlType, uiauto_IUIAutomationElement_CurrentControlType, uiautomationclient/IUIAutomationElement::CurrentControlType, uiautomationclient/IUIAutomationElement::get_CurrentControlType, winauto.uiauto_IUIAutomationElement_CurrentControlType
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationElement::get_CurrentControlType
 - uiautomationclient/IUIAutomationElement::get_CurrentControlType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationElement.CurrentControlType
 - IUIAutomationElement.get_CurrentControlType
---

# IUIAutomationElement::get_CurrentControlType


## -description

Retrieves the control type of the element.

This property is read-only.

## -parameters

## -remarks

Control types describe a known interaction model for UI Automation elements without relying on a localized control type or combination of complex logic rules.
This property cannot change at run time unless the control supports the <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationmultipleviewpattern">IUIAutomationMultipleViewPattern</a> interface. An example is the Win32 ListView control, which can change from a data grid to a list, depending on the current view.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-automation-element-propids">Automation Element Property IDs</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype">CachedControlType</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>



<b>Reference</b>