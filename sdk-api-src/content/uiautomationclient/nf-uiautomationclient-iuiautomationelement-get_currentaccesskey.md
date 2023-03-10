---
UID: NF:uiautomationclient.IUIAutomationElement.get_CurrentAccessKey
title: IUIAutomationElement::get_CurrentAccessKey (uiautomationclient.h)
description: Retrieves the access key character for the element.
helpviewer_keywords: ["CurrentAccessKey property [Windows Accessibility]","CurrentAccessKey property [Windows Accessibility]","IUIAutomationElement interface","IUIAutomationElement interface [Windows Accessibility]","CurrentAccessKey property","IUIAutomationElement.CurrentAccessKey","IUIAutomationElement.get_CurrentAccessKey","IUIAutomationElement::CurrentAccessKey","IUIAutomationElement::get_CurrentAccessKey","get_CurrentAccessKey","uiauto.uiauto_IUIAutomationElement_CurrentAccessKey","uiauto_IUIAutomationElement_CurrentAccessKey","uiautomationclient/IUIAutomationElement::CurrentAccessKey","uiautomationclient/IUIAutomationElement::get_CurrentAccessKey","winauto.uiauto_IUIAutomationElement_CurrentAccessKey"]
old-location: winauto\uiauto_IUIAutomationElement_CurrentAccessKey.htm
tech.root: WinAuto
ms.assetid: 0da10db5-a978-4575-86c4-12152691468f
ms.date: 12/05/2018
ms.keywords: CurrentAccessKey property [Windows Accessibility], CurrentAccessKey property [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],CurrentAccessKey property, IUIAutomationElement.CurrentAccessKey, IUIAutomationElement.get_CurrentAccessKey, IUIAutomationElement::CurrentAccessKey, IUIAutomationElement::get_CurrentAccessKey, get_CurrentAccessKey, uiauto.uiauto_IUIAutomationElement_CurrentAccessKey, uiauto_IUIAutomationElement_CurrentAccessKey, uiautomationclient/IUIAutomationElement::CurrentAccessKey, uiautomationclient/IUIAutomationElement::get_CurrentAccessKey, winauto.uiauto_IUIAutomationElement_CurrentAccessKey
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
 - IUIAutomationElement::get_CurrentAccessKey
 - uiautomationclient/IUIAutomationElement::get_CurrentAccessKey
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
 - IUIAutomationElement.CurrentAccessKey
 - IUIAutomationElement.get_CurrentAccessKey
---

# IUIAutomationElement::get_CurrentAccessKey


## -description

Retrieves the access key character for the element.

This property is read-only.

## -parameters

## -remarks

An access key is a character in the text of a menu, menu item, or label of a control such as a button that activates the attached menu function. For example, the letter "O" is often used to invoke the Open file common dialog box from a File menu. Microsoft UI Automation elements that have the access key property set always implement the <a href="/windows/desktop/WinAuto/uiauto-implementinginvoke">Invoke</a> control pattern.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-automation-element-propids">Automation Element Property IDs</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedaccesskey">CachedAccessKey</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>



<b>Reference</b>