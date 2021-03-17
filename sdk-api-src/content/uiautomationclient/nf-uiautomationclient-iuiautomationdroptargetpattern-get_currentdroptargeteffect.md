---
UID: NF:uiautomationclient.IUIAutomationDropTargetPattern.get_CurrentDropTargetEffect
title: IUIAutomationDropTargetPattern::get_CurrentDropTargetEffect (uiautomationclient.h)
description: Retrieves a localized string that describes what happens when the user drops the grabbed element on this drop target.
helpviewer_keywords: ["CurrentDropTargetEffect property [Windows Accessibility]","CurrentDropTargetEffect property [Windows Accessibility]","IUIAutomationDropTargetPattern interface","IUIAutomationDropTargetPattern interface [Windows Accessibility]","CurrentDropTargetEffect property","IUIAutomationDropTargetPattern.CurrentDropTargetEffect","IUIAutomationDropTargetPattern.get_CurrentDropTargetEffect","IUIAutomationDropTargetPattern::CurrentDropTargetEffect","IUIAutomationDropTargetPattern::get_CurrentDropTargetEffect","get_CurrentDropTargetEffect","uiautomationclient/IUIAutomationDropTargetPattern::CurrentDropTargetEffect","uiautomationclient/IUIAutomationDropTargetPattern::get_CurrentDropTargetEffect","winauto.uiauto_iuiautomationdroptargetpattern_currentdroptargeteffect"]
old-location: winauto\uiauto_iuiautomationdroptargetpattern_currentdroptargeteffect.htm
tech.root: WinAuto
ms.assetid: C7A2C62B-D61B-4884-BEF0-E4EB1088D1AB
ms.date: 12/05/2018
ms.keywords: CurrentDropTargetEffect property [Windows Accessibility], CurrentDropTargetEffect property [Windows Accessibility],IUIAutomationDropTargetPattern interface, IUIAutomationDropTargetPattern interface [Windows Accessibility],CurrentDropTargetEffect property, IUIAutomationDropTargetPattern.CurrentDropTargetEffect, IUIAutomationDropTargetPattern.get_CurrentDropTargetEffect, IUIAutomationDropTargetPattern::CurrentDropTargetEffect, IUIAutomationDropTargetPattern::get_CurrentDropTargetEffect, get_CurrentDropTargetEffect, uiautomationclient/IUIAutomationDropTargetPattern::CurrentDropTargetEffect, uiautomationclient/IUIAutomationDropTargetPattern::get_CurrentDropTargetEffect, winauto.uiauto_iuiautomationdroptargetpattern_currentdroptargeteffect
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationDropTargetPattern::get_CurrentDropTargetEffect
 - uiautomationclient/IUIAutomationDropTargetPattern::get_CurrentDropTargetEffect
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
 - IUIAutomationDropTargetPattern.CurrentDropTargetEffect
 - IUIAutomationDropTargetPattern.get_CurrentDropTargetEffect
---

# IUIAutomationDropTargetPattern::get_CurrentDropTargetEffect


## -description

Retrieves a localized string that describes what happens when the user drops the grabbed element on this drop target.

This property is read-only.

## -parameters

## -remarks

This property describes the default effect that happens when the user drops a grabbed element on a target, such as moving or copying the element.  This property can be a short string such as "move", or a longer one such as "insert into Main group".  The string is always localized.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationdroptargetpattern">IUIAutomationDropTargetPattern</a>