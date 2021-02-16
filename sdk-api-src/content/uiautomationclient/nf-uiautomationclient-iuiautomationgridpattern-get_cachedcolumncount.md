---
UID: NF:uiautomationclient.IUIAutomationGridPattern.get_CachedColumnCount
title: IUIAutomationGridPattern::get_CachedColumnCount (uiautomationclient.h)
description: Retrieves the cached number of columns in the grid.
helpviewer_keywords: ["CachedColumnCount property [Windows Accessibility]","CachedColumnCount property [Windows Accessibility]","IUIAutomationGridPattern interface","IUIAutomationGridPattern interface [Windows Accessibility]","CachedColumnCount property","IUIAutomationGridPattern.CachedColumnCount","IUIAutomationGridPattern.get_CachedColumnCount","IUIAutomationGridPattern::CachedColumnCount","IUIAutomationGridPattern::get_CachedColumnCount","get_CachedColumnCount","uiauto.uiauto_IUIAutomationGridPattern_CachedColumnCount","uiauto_IUIAutomationGridPattern_CachedColumnCount","uiautomationclient/IUIAutomationGridPattern::CachedColumnCount","uiautomationclient/IUIAutomationGridPattern::get_CachedColumnCount","winauto.uiauto_IUIAutomationGridPattern_CachedColumnCount"]
old-location: winauto\uiauto_IUIAutomationGridPattern_CachedColumnCount.htm
tech.root: WinAuto
ms.assetid: d425d767-3ae4-4644-a8bb-b901462c6c4b
ms.date: 12/05/2018
ms.keywords: CachedColumnCount property [Windows Accessibility], CachedColumnCount property [Windows Accessibility],IUIAutomationGridPattern interface, IUIAutomationGridPattern interface [Windows Accessibility],CachedColumnCount property, IUIAutomationGridPattern.CachedColumnCount, IUIAutomationGridPattern.get_CachedColumnCount, IUIAutomationGridPattern::CachedColumnCount, IUIAutomationGridPattern::get_CachedColumnCount, get_CachedColumnCount, uiauto.uiauto_IUIAutomationGridPattern_CachedColumnCount, uiauto_IUIAutomationGridPattern_CachedColumnCount, uiautomationclient/IUIAutomationGridPattern::CachedColumnCount, uiautomationclient/IUIAutomationGridPattern::get_CachedColumnCount, winauto.uiauto_IUIAutomationGridPattern_CachedColumnCount
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
 - IUIAutomationGridPattern::get_CachedColumnCount
 - uiautomationclient/IUIAutomationGridPattern::get_CachedColumnCount
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
 - IUIAutomationGridPattern.CachedColumnCount
 - IUIAutomationGridPattern.get_CachedColumnCount
---

# IUIAutomationGridPattern::get_CachedColumnCount


## -description

Retrieves the cached number of columns in the grid.

This property is read-only.

## -parameters

## -remarks

Hidden rows and columns, depending on the provider implementation, may be loaded in the Microsoft UI Automation tree and will therefore be reflected in the row count and column count properties. If the hidden rows and columns have not yet been loaded they are not counted.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationgridpattern">IUIAutomationGridPattern</a>