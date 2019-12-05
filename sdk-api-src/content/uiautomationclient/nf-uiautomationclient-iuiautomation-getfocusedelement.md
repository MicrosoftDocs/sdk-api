---
UID: NF:uiautomationclient.IUIAutomation.GetFocusedElement
title: IUIAutomation::GetFocusedElement (uiautomationclient.h)
description: Retrieves the UI Automation element that has the input focus.
old-location: winauto\uiauto_IUIAutomation_GetFocusedElement.htm
tech.root: WinAuto
ms.assetid: a75f03bc-f472-40bf-8fa2-8c1d3ddf4fbb
ms.date: 12/05/2018
ms.keywords: GetFocusedElement, GetFocusedElement method [Windows Accessibility], GetFocusedElement method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],GetFocusedElement method, IUIAutomation.GetFocusedElement, IUIAutomation::GetFocusedElement, uiauto.uiauto_IUIAutomation_GetFocusedElement, uiauto_IUIAutomation_GetFocusedElement, uiautomationclient/IUIAutomation::GetFocusedElement, winauto.uiauto_IUIAutomation_GetFocusedElement
ms.topic: method
f1_keywords:
- uiautomationclient/IUIAutomation.GetFocusedElement
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- UIAutomationClient.h
api_name:
- IUIAutomation.GetFocusedElement
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomation::GetFocusedElement


## -description


Retrieves the UI Automation element that has the input focus.


## -parameters




### -param element [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>**</b>

Receives a pointer to the UI Automation element.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>IUIAutomation::GetFocusedElement</b> method returns the <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-error-codes">UIA_E_ELEMENTNOTAVAILABLE</a> error code if the focused element is already removed by the time the method returns. Clients should handle errors from this method gracefully; for example, by trying the call again.
			



