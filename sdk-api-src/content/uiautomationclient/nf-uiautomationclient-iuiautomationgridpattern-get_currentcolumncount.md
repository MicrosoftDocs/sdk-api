---
UID: NF:uiautomationclient.IUIAutomationGridPattern.get_CurrentColumnCount
title: IUIAutomationGridPattern::get_CurrentColumnCount (uiautomationclient.h)
description: The number of columns in the grid.
helpviewer_keywords: ["CurrentColumnCount property [Windows Accessibility]","CurrentColumnCount property [Windows Accessibility]","IUIAutomationGridPattern interface","IUIAutomationGridPattern interface [Windows Accessibility]","CurrentColumnCount property","IUIAutomationGridPattern.CurrentColumnCount","IUIAutomationGridPattern.get_CurrentColumnCount","IUIAutomationGridPattern::CurrentColumnCount","IUIAutomationGridPattern::get_CurrentColumnCount","get_CurrentColumnCount","uiauto.uiauto_IUIAutomationGridPattern_CurrentColumnCount","uiauto_IUIAutomationGridPattern_CurrentColumnCount","uiautomationclient/IUIAutomationGridPattern::CurrentColumnCount","uiautomationclient/IUIAutomationGridPattern::get_CurrentColumnCount","winauto.uiauto_IUIAutomationGridPattern_CurrentColumnCount"]
old-location: winauto\uiauto_IUIAutomationGridPattern_CurrentColumnCount.htm
tech.root: WinAuto
ms.assetid: bbacb1a5-aca4-4a1b-ad2e-ff55b32ac395
ms.date: 12/05/2018
ms.keywords: CurrentColumnCount property [Windows Accessibility], CurrentColumnCount property [Windows Accessibility],IUIAutomationGridPattern interface, IUIAutomationGridPattern interface [Windows Accessibility],CurrentColumnCount property, IUIAutomationGridPattern.CurrentColumnCount, IUIAutomationGridPattern.get_CurrentColumnCount, IUIAutomationGridPattern::CurrentColumnCount, IUIAutomationGridPattern::get_CurrentColumnCount, get_CurrentColumnCount, uiauto.uiauto_IUIAutomationGridPattern_CurrentColumnCount, uiauto_IUIAutomationGridPattern_CurrentColumnCount, uiautomationclient/IUIAutomationGridPattern::CurrentColumnCount, uiautomationclient/IUIAutomationGridPattern::get_CurrentColumnCount, winauto.uiauto_IUIAutomationGridPattern_CurrentColumnCount
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
 - IUIAutomationGridPattern::get_CurrentColumnCount
 - uiautomationclient/IUIAutomationGridPattern::get_CurrentColumnCount
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
 - IUIAutomationGridPattern.CurrentColumnCount
 - IUIAutomationGridPattern.get_CurrentColumnCount
---

# IUIAutomationGridPattern::get_CurrentColumnCount


## -description

The number of columns in the grid.

This property is read-only.

## -parameters

## -remarks

Hidden rows and columns, depending on the provider implementation, may be loaded in the Microsoft UI Automation tree and will therefore be reflected in the row count and column count properties. If the hidden rows and columns have not yet been loaded they are not counted.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationgridpattern">IUIAutomationGridPattern</a>