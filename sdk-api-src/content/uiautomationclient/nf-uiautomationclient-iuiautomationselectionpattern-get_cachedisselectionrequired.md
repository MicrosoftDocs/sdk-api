---
UID: NF:uiautomationclient.IUIAutomationSelectionPattern.get_CachedIsSelectionRequired
title: IUIAutomationSelectionPattern::get_CachedIsSelectionRequired (uiautomationclient.h)
description: Retrieves a cached value that indicates whether at least one item must be selected at all times.
helpviewer_keywords: ["CachedIsSelectionRequired property [Windows Accessibility]","CachedIsSelectionRequired property [Windows Accessibility]","IUIAutomationSelectionPattern interface","IUIAutomationSelectionPattern interface [Windows Accessibility]","CachedIsSelectionRequired property","IUIAutomationSelectionPattern.CachedIsSelectionRequired","IUIAutomationSelectionPattern.get_CachedIsSelectionRequired","IUIAutomationSelectionPattern::CachedIsSelectionRequired","IUIAutomationSelectionPattern::get_CachedIsSelectionRequired","get_CachedIsSelectionRequired","uiauto.uiauto_IUIAutomationSelectionPattern_CachedIsSelectionRequired","uiauto_IUIAutomationSelectionPattern_CachedIsSelectionRequired","uiautomationclient/IUIAutomationSelectionPattern::CachedIsSelectionRequired","uiautomationclient/IUIAutomationSelectionPattern::get_CachedIsSelectionRequired","winauto.uiauto_IUIAutomationSelectionPattern_CachedIsSelectionRequired"]
old-location: winauto\uiauto_IUIAutomationSelectionPattern_CachedIsSelectionRequired.htm
tech.root: WinAuto
ms.assetid: 74846653-bf18-4289-9ad8-aedc20a56f29
ms.date: 12/05/2018
ms.keywords: CachedIsSelectionRequired property [Windows Accessibility], CachedIsSelectionRequired property [Windows Accessibility],IUIAutomationSelectionPattern interface, IUIAutomationSelectionPattern interface [Windows Accessibility],CachedIsSelectionRequired property, IUIAutomationSelectionPattern.CachedIsSelectionRequired, IUIAutomationSelectionPattern.get_CachedIsSelectionRequired, IUIAutomationSelectionPattern::CachedIsSelectionRequired, IUIAutomationSelectionPattern::get_CachedIsSelectionRequired, get_CachedIsSelectionRequired, uiauto.uiauto_IUIAutomationSelectionPattern_CachedIsSelectionRequired, uiauto_IUIAutomationSelectionPattern_CachedIsSelectionRequired, uiautomationclient/IUIAutomationSelectionPattern::CachedIsSelectionRequired, uiautomationclient/IUIAutomationSelectionPattern::get_CachedIsSelectionRequired, winauto.uiauto_IUIAutomationSelectionPattern_CachedIsSelectionRequired
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
 - IUIAutomationSelectionPattern::get_CachedIsSelectionRequired
 - uiautomationclient/IUIAutomationSelectionPattern::get_CachedIsSelectionRequired
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
 - IUIAutomationSelectionPattern.CachedIsSelectionRequired
 - IUIAutomationSelectionPattern.get_CachedIsSelectionRequired
---

# IUIAutomationSelectionPattern::get_CachedIsSelectionRequired


## -description

Retrieves a cached value that indicates whether at least one item must be selected at all times.

This property is read-only.

## -parameters

## -remarks

This property can be dynamic. For example, the initial state of a control might not have any items selected by default, but after an item is selected, the control must always have at least one item selected.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationselectionpattern">IUIAutomationSelectionPattern</a>