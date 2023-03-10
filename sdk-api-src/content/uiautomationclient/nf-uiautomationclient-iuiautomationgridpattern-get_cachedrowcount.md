---
UID: NF:uiautomationclient.IUIAutomationGridPattern.get_CachedRowCount
title: IUIAutomationGridPattern::get_CachedRowCount (uiautomationclient.h)
description: Retrieves the cached number of rows in the grid.
helpviewer_keywords: ["CachedRowCount property [Windows Accessibility]","CachedRowCount property [Windows Accessibility]","IUIAutomationGridPattern interface","IUIAutomationGridPattern interface [Windows Accessibility]","CachedRowCount property","IUIAutomationGridPattern.CachedRowCount","IUIAutomationGridPattern.get_CachedRowCount","IUIAutomationGridPattern::CachedRowCount","IUIAutomationGridPattern::get_CachedRowCount","get_CachedRowCount","uiauto.uiauto_IUIAutomationGridPattern_CachedRowCount","uiauto_IUIAutomationGridPattern_CachedRowCount","uiautomationclient/IUIAutomationGridPattern::CachedRowCount","uiautomationclient/IUIAutomationGridPattern::get_CachedRowCount","winauto.uiauto_IUIAutomationGridPattern_CachedRowCount"]
old-location: winauto\uiauto_IUIAutomationGridPattern_CachedRowCount.htm
tech.root: WinAuto
ms.assetid: 783e48e4-c554-4bc9-bf36-3fcc35d00d22
ms.date: 12/05/2018
ms.keywords: CachedRowCount property [Windows Accessibility], CachedRowCount property [Windows Accessibility],IUIAutomationGridPattern interface, IUIAutomationGridPattern interface [Windows Accessibility],CachedRowCount property, IUIAutomationGridPattern.CachedRowCount, IUIAutomationGridPattern.get_CachedRowCount, IUIAutomationGridPattern::CachedRowCount, IUIAutomationGridPattern::get_CachedRowCount, get_CachedRowCount, uiauto.uiauto_IUIAutomationGridPattern_CachedRowCount, uiauto_IUIAutomationGridPattern_CachedRowCount, uiautomationclient/IUIAutomationGridPattern::CachedRowCount, uiautomationclient/IUIAutomationGridPattern::get_CachedRowCount, winauto.uiauto_IUIAutomationGridPattern_CachedRowCount
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
 - IUIAutomationGridPattern::get_CachedRowCount
 - uiautomationclient/IUIAutomationGridPattern::get_CachedRowCount
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
 - IUIAutomationGridPattern.CachedRowCount
 - IUIAutomationGridPattern.get_CachedRowCount
---

# IUIAutomationGridPattern::get_CachedRowCount


## -description

Retrieves the cached number of rows in the grid.

This property is read-only.

## -parameters

## -remarks

Hidden rows and columns, depending on the provider implementation, may be loaded in the Microsoft UI Automation tree and will therefore be reflected in the row count and column count properties. If the hidden rows and columns have not yet been loaded they are not counted.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationgridpattern">IUIAutomationGridPattern</a>