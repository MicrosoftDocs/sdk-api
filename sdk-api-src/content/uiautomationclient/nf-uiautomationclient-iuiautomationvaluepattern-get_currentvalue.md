---
UID: NF:uiautomationclient.IUIAutomationValuePattern.get_CurrentValue
title: IUIAutomationValuePattern::get_CurrentValue (uiautomationclient.h)
description: Retrieves the value of the element.
helpviewer_keywords: ["CurrentValue property [Windows Accessibility]","CurrentValue property [Windows Accessibility]","IUIAutomationValuePattern interface","IUIAutomationValuePattern interface [Windows Accessibility]","CurrentValue property","IUIAutomationValuePattern.CurrentValue","IUIAutomationValuePattern.get_CurrentValue","IUIAutomationValuePattern::CurrentValue","IUIAutomationValuePattern::get_CurrentValue","get_CurrentValue","uiauto.uiauto_IUIAutomationValuePattern_CurrentValue","uiauto_IUIAutomationValuePattern_CurrentValue","uiautomationclient/IUIAutomationValuePattern::CurrentValue","uiautomationclient/IUIAutomationValuePattern::get_CurrentValue","winauto.uiauto_IUIAutomationValuePattern_CurrentValue"]
old-location: winauto\uiauto_IUIAutomationValuePattern_CurrentValue.htm
tech.root: WinAuto
ms.assetid: df7d4e74-34d1-435c-86cd-a8fee52f6a94
ms.date: 12/05/2018
ms.keywords: CurrentValue property [Windows Accessibility], CurrentValue property [Windows Accessibility],IUIAutomationValuePattern interface, IUIAutomationValuePattern interface [Windows Accessibility],CurrentValue property, IUIAutomationValuePattern.CurrentValue, IUIAutomationValuePattern.get_CurrentValue, IUIAutomationValuePattern::CurrentValue, IUIAutomationValuePattern::get_CurrentValue, get_CurrentValue, uiauto.uiauto_IUIAutomationValuePattern_CurrentValue, uiauto_IUIAutomationValuePattern_CurrentValue, uiautomationclient/IUIAutomationValuePattern::CurrentValue, uiautomationclient/IUIAutomationValuePattern::get_CurrentValue, winauto.uiauto_IUIAutomationValuePattern_CurrentValue
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
 - IUIAutomationValuePattern::get_CurrentValue
 - uiautomationclient/IUIAutomationValuePattern::get_CurrentValue
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
 - IUIAutomationValuePattern.CurrentValue
 - IUIAutomationValuePattern.get_CurrentValue
---

# IUIAutomationValuePattern::get_CurrentValue


## -description

Retrieves the value of the element.

This property is read-only.

## -parameters

## -remarks

Single-line edit controls support programmatic access to their contents through <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationvaluepattern">IUIAutomationValuePattern</a>. However, multiline edit controls do not support this control pattern, and their contents must be retrieved by using <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextpattern">IUIAutomationTextPattern</a>.

This property does not support the retrieval of formatting information or substring values. <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextpattern">IUIAutomationTextPattern</a> must be used in these scenarios as well.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationvaluepattern">IUIAutomationValuePattern</a>