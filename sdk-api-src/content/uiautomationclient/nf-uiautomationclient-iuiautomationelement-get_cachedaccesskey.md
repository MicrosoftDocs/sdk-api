---
UID: NF:uiautomationclient.IUIAutomationElement.get_CachedAccessKey
title: IUIAutomationElement::get_CachedAccessKey (uiautomationclient.h)
description: Retrieves the cached access key character for the element.
helpviewer_keywords: ["CachedAccessKey property [Windows Accessibility]","CachedAccessKey property [Windows Accessibility]","IUIAutomationElement interface","IUIAutomationElement interface [Windows Accessibility]","CachedAccessKey property","IUIAutomationElement.CachedAccessKey","IUIAutomationElement.get_CachedAccessKey","IUIAutomationElement::CachedAccessKey","IUIAutomationElement::get_CachedAccessKey","get_CachedAccessKey","uiauto.uiauto_IUIAutomationElement_CachedAccessKey","uiauto_IUIAutomationElement_CachedAccessKey","uiautomationclient/IUIAutomationElement::CachedAccessKey","uiautomationclient/IUIAutomationElement::get_CachedAccessKey","winauto.uiauto_IUIAutomationElement_CachedAccessKey"]
old-location: winauto\uiauto_IUIAutomationElement_CachedAccessKey.htm
tech.root: WinAuto
ms.assetid: dc4394b3-f609-4709-b9b5-c8bf84d17b3f
ms.date: 12/05/2018
ms.keywords: CachedAccessKey property [Windows Accessibility], CachedAccessKey property [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],CachedAccessKey property, IUIAutomationElement.CachedAccessKey, IUIAutomationElement.get_CachedAccessKey, IUIAutomationElement::CachedAccessKey, IUIAutomationElement::get_CachedAccessKey, get_CachedAccessKey, uiauto.uiauto_IUIAutomationElement_CachedAccessKey, uiauto_IUIAutomationElement_CachedAccessKey, uiautomationclient/IUIAutomationElement::CachedAccessKey, uiautomationclient/IUIAutomationElement::get_CachedAccessKey, winauto.uiauto_IUIAutomationElement_CachedAccessKey
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IUIAutomationElement::get_CachedAccessKey
 - uiautomationclient/IUIAutomationElement::get_CachedAccessKey
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
 - IUIAutomationElement.CachedAccessKey
 - IUIAutomationElement.get_CachedAccessKey
---

# IUIAutomationElement::get_CachedAccessKey


## -description

Retrieves the cached access key character for the element.

This property is read-only.

## -parameters

## -remarks

An access key is a character in the text of a menu, menu item, or label of a control such as a button that activates the attached menu function. For example, the letter "O" is often used to invoke the Open file common dialog box from a File menu. Microsoft UI Automation elements that have the access key property set always implement the <a href="/windows/desktop/WinAuto/uiauto-implementinginvoke">Invoke</a> control pattern.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-automation-element-propids">Automation Element Property IDs</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentaccesskey">CurrentAccessKey</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>



<b>Reference</b>