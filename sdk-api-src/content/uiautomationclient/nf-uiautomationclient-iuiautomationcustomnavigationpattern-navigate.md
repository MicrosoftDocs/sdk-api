---
UID: NF:uiautomationclient.IUIAutomationCustomNavigationPattern.Navigate
title: IUIAutomationCustomNavigationPattern::Navigate (uiautomationclient.h)
description: Gets the next element in the specified direction within the logical UI tree.
helpviewer_keywords: ["IUIAutomationCustomNavigationPattern interface [Windows Accessibility]","Navigate method","IUIAutomationCustomNavigationPattern.Navigate","IUIAutomationCustomNavigationPattern::Navigate","Navigate","Navigate method [Windows Accessibility]","Navigate method [Windows Accessibility]","IUIAutomationCustomNavigationPattern interface","uiautomationclient/IUIAutomationCustomNavigationPattern::Navigate","winauto.uiauto_IUIAutomationCustomNavigationPattern_Navigate"]
old-location: winauto\uiauto_IUIAutomationCustomNavigationPattern_Navigate.htm
tech.root: WinAuto
ms.assetid: 82481F62-9FBB-42C8-BDCB-2462FEEB5A0F
ms.date: 12/05/2018
ms.keywords: IUIAutomationCustomNavigationPattern interface [Windows Accessibility],Navigate method, IUIAutomationCustomNavigationPattern.Navigate, IUIAutomationCustomNavigationPattern::Navigate, Navigate, Navigate method [Windows Accessibility], Navigate method [Windows Accessibility],IUIAutomationCustomNavigationPattern interface, uiautomationclient/IUIAutomationCustomNavigationPattern::Navigate, winauto.uiauto_IUIAutomationCustomNavigationPattern_Navigate
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IUIAutomationCustomNavigationPattern::Navigate
 - uiautomationclient/IUIAutomationCustomNavigationPattern::Navigate
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
 - IUIAutomationCustomNavigationPattern.Navigate
---

# IUIAutomationCustomNavigationPattern::Navigate


## -description

Gets the next element in the specified direction within the logical UI tree.

## -parameters

### -param direction [in]

The specified direction.

### -param pRetVal [out, retval]

The next element as specified by the <i>direction</i> parameter.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcustomnavigationpattern">IUIAutomationCustomNavigationPattern</a>