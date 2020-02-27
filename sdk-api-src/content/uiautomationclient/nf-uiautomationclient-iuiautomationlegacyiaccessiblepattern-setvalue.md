---
UID: NF:uiautomationclient.IUIAutomationLegacyIAccessiblePattern.SetValue
title: IUIAutomationLegacyIAccessiblePattern::SetValue (uiautomationclient.h)
description: Sets the Microsoft Active Accessibility value property for the element.
old-location: winauto\uiauto_IUIAutomationLegacyIAccessiblePattern_SetValue.htm
tech.root: WinAuto
ms.assetid: c5891bb3-e727-430c-a4d4-5c59750b01ce
ms.date: 12/05/2018
ms.keywords: IUIAutomationLegacyIAccessiblePattern interface [Windows Accessibility],SetValue method, IUIAutomationLegacyIAccessiblePattern.SetValue, IUIAutomationLegacyIAccessiblePattern::SetValue, SetValue, SetValue method [Windows Accessibility], SetValue method [Windows Accessibility],IUIAutomationLegacyIAccessiblePattern interface, uiauto.uiauto_IUIAutomationLegacyIAccessiblePattern_SetValue, uiauto_IUIAutomationLegacyIAccessiblePattern_SetValue, uiautomationclient/IUIAutomationLegacyIAccessiblePattern::SetValue, winauto.uiauto_IUIAutomationLegacyIAccessiblePattern_SetValue
f1_keywords:
- uiautomationclient/IUIAutomationLegacyIAccessiblePattern.SetValue
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- UIAutomationClient.h
api_name:
- IUIAutomationLegacyIAccessiblePattern.SetValue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationLegacyIAccessiblePattern::SetValue


## -description


Sets the Microsoft Active Accessibility value property for the element.


## -parameters




### -param szValue

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">LPCWSTR</a></b>

A localized string that contains the object's value.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is supported only for some elements (usually edit controls). 
			




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern">IUIAutomationLegacyIAccessiblePattern</a>
 

 

