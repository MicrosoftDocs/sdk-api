---
UID: NF:uiautomationclient.IUIAutomationElement.get_CachedControlType
title: IUIAutomationElement::get_CachedControlType (uiautomationclient.h)
description: Retrieves a cached value that indicates the control type of the element.
helpviewer_keywords: ["CachedControlType property [Windows Accessibility]","CachedControlType property [Windows Accessibility]","IUIAutomationElement interface","IUIAutomationElement interface [Windows Accessibility]","CachedControlType property","IUIAutomationElement.CachedControlType","IUIAutomationElement.get_CachedControlType","IUIAutomationElement::CachedControlType","IUIAutomationElement::get_CachedControlType","get_CachedControlType","uiauto.uiauto_IUIAutomationElement_CachedControlType","uiauto_IUIAutomationElement_CachedControlType","uiautomationclient/IUIAutomationElement::CachedControlType","uiautomationclient/IUIAutomationElement::get_CachedControlType","winauto.uiauto_IUIAutomationElement_CachedControlType"]
old-location: winauto\uiauto_IUIAutomationElement_CachedControlType.htm
tech.root: WinAuto
ms.assetid: 48b232a8-8826-4c70-b541-3e6a792105c1
ms.date: 12/05/2018
ms.keywords: CachedControlType property [Windows Accessibility], CachedControlType property [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],CachedControlType property, IUIAutomationElement.CachedControlType, IUIAutomationElement.get_CachedControlType, IUIAutomationElement::CachedControlType, IUIAutomationElement::get_CachedControlType, get_CachedControlType, uiauto.uiauto_IUIAutomationElement_CachedControlType, uiauto_IUIAutomationElement_CachedControlType, uiautomationclient/IUIAutomationElement::CachedControlType, uiautomationclient/IUIAutomationElement::get_CachedControlType, winauto.uiauto_IUIAutomationElement_CachedControlType
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
 - IUIAutomationElement::get_CachedControlType
 - uiautomationclient/IUIAutomationElement::get_CachedControlType
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
 - IUIAutomationElement.CachedControlType
 - IUIAutomationElement.get_CachedControlType
---

# IUIAutomationElement::get_CachedControlType


## -description

Retrieves a cached value that indicates the control type of the element.

This property is read-only.

## -parameters

## -remarks

Control types describe a known interaction model for UI Automation elements without relying on a localized control type or combination of complex logic rules. This property cannot change at run time unless the control supports the <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationmultipleviewpattern">IUIAutomationMultipleViewPattern</a> interface. An example is the Win32 ListView control, which can change from a data grid to a list, depending on the current view.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-automation-element-propids">Automation Element Property IDs</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype">CurrentControlType</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>



<b>Reference</b>