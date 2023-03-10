---
UID: NF:uiautomationclient.IUIAutomationSelectionPattern.get_CurrentIsSelectionRequired
title: IUIAutomationSelectionPattern::get_CurrentIsSelectionRequired (uiautomationclient.h)
description: Indicates whether at least one item must be selected at all times.
helpviewer_keywords: ["CurrentIsSelectionRequired property [Windows Accessibility]","CurrentIsSelectionRequired property [Windows Accessibility]","IUIAutomationSelectionPattern interface","IUIAutomationSelectionPattern interface [Windows Accessibility]","CurrentIsSelectionRequired property","IUIAutomationSelectionPattern.CurrentIsSelectionRequired","IUIAutomationSelectionPattern.get_CurrentIsSelectionRequired","IUIAutomationSelectionPattern::CurrentIsSelectionRequired","IUIAutomationSelectionPattern::get_CurrentIsSelectionRequired","get_CurrentIsSelectionRequired","uiauto.uiauto_IUIAutomationSelectionPattern_CurrentIsSelectionRequired","uiauto_IUIAutomationSelectionPattern_CurrentIsSelectionRequired","uiautomationclient/IUIAutomationSelectionPattern::CurrentIsSelectionRequired","uiautomationclient/IUIAutomationSelectionPattern::get_CurrentIsSelectionRequired","winauto.uiauto_IUIAutomationSelectionPattern_CurrentIsSelectionRequired"]
old-location: winauto\uiauto_IUIAutomationSelectionPattern_CurrentIsSelectionRequired.htm
tech.root: WinAuto
ms.assetid: 608c9b6d-bc53-4d6d-8747-897ac9a24571
ms.date: 12/05/2018
ms.keywords: CurrentIsSelectionRequired property [Windows Accessibility], CurrentIsSelectionRequired property [Windows Accessibility],IUIAutomationSelectionPattern interface, IUIAutomationSelectionPattern interface [Windows Accessibility],CurrentIsSelectionRequired property, IUIAutomationSelectionPattern.CurrentIsSelectionRequired, IUIAutomationSelectionPattern.get_CurrentIsSelectionRequired, IUIAutomationSelectionPattern::CurrentIsSelectionRequired, IUIAutomationSelectionPattern::get_CurrentIsSelectionRequired, get_CurrentIsSelectionRequired, uiauto.uiauto_IUIAutomationSelectionPattern_CurrentIsSelectionRequired, uiauto_IUIAutomationSelectionPattern_CurrentIsSelectionRequired, uiautomationclient/IUIAutomationSelectionPattern::CurrentIsSelectionRequired, uiautomationclient/IUIAutomationSelectionPattern::get_CurrentIsSelectionRequired, winauto.uiauto_IUIAutomationSelectionPattern_CurrentIsSelectionRequired
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
 - IUIAutomationSelectionPattern::get_CurrentIsSelectionRequired
 - uiautomationclient/IUIAutomationSelectionPattern::get_CurrentIsSelectionRequired
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
 - IUIAutomationSelectionPattern.CurrentIsSelectionRequired
 - IUIAutomationSelectionPattern.get_CurrentIsSelectionRequired
---

# IUIAutomationSelectionPattern::get_CurrentIsSelectionRequired


## -description

Indicates whether at least one item must be selected at all times.

This property is read-only.

## -parameters

## -remarks

This property can be dynamic. For example, the initial state of a control might not have any items selected by default, but after an item is selected, the control must always have at least one item selected.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationselectionpattern">IUIAutomationSelectionPattern</a>