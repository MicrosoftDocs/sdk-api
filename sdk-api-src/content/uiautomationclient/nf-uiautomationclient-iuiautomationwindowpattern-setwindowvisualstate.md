---
UID: NF:uiautomationclient.IUIAutomationWindowPattern.SetWindowVisualState
title: IUIAutomationWindowPattern::SetWindowVisualState (uiautomationclient.h)
description: Minimizes, maximizes, or restores the window.
helpviewer_keywords: ["IUIAutomationWindowPattern interface [Windows Accessibility]","SetWindowVisualState method","IUIAutomationWindowPattern.SetWindowVisualState","IUIAutomationWindowPattern::SetWindowVisualState","SetWindowVisualState","SetWindowVisualState method [Windows Accessibility]","SetWindowVisualState method [Windows Accessibility]","IUIAutomationWindowPattern interface","uiauto.uiauto_IUIAutomationWindowPattern_SetWindowVisualState","uiauto_IUIAutomationWindowPattern_SetWindowVisualState","uiautomationclient/IUIAutomationWindowPattern::SetWindowVisualState","winauto.uiauto_IUIAutomationWindowPattern_SetWindowVisualState"]
old-location: winauto\uiauto_IUIAutomationWindowPattern_SetWindowVisualState.htm
tech.root: WinAuto
ms.assetid: 106322f8-cf43-48ca-8bc4-f51a75731127
ms.date: 12/05/2018
ms.keywords: IUIAutomationWindowPattern interface [Windows Accessibility],SetWindowVisualState method, IUIAutomationWindowPattern.SetWindowVisualState, IUIAutomationWindowPattern::SetWindowVisualState, SetWindowVisualState, SetWindowVisualState method [Windows Accessibility], SetWindowVisualState method [Windows Accessibility],IUIAutomationWindowPattern interface, uiauto.uiauto_IUIAutomationWindowPattern_SetWindowVisualState, uiauto_IUIAutomationWindowPattern_SetWindowVisualState, uiautomationclient/IUIAutomationWindowPattern::SetWindowVisualState, winauto.uiauto_IUIAutomationWindowPattern_SetWindowVisualState
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
 - IUIAutomationWindowPattern::SetWindowVisualState
 - uiautomationclient/IUIAutomationWindowPattern::SetWindowVisualState
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
 - IUIAutomationWindowPattern.SetWindowVisualState
---

# IUIAutomationWindowPattern::SetWindowVisualState


## -description

Minimizes, maximizes, or restores the window.

## -parameters

### -param state [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-windowvisualstate">WindowVisualState</a></b>

The new visual state of the window.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationwindowpattern">IUIAutomationWindowPattern</a>