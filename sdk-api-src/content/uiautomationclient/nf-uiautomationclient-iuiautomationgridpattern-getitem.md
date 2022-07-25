---
UID: NF:uiautomationclient.IUIAutomationGridPattern.GetItem
title: IUIAutomationGridPattern::GetItem (uiautomationclient.h)
description: Retrieves a UI Automation element representing an item in the grid.
helpviewer_keywords: ["GetItem","GetItem method [Windows Accessibility]","GetItem method [Windows Accessibility]","IUIAutomationGridPattern interface","IUIAutomationGridPattern interface [Windows Accessibility]","GetItem method","IUIAutomationGridPattern.GetItem","IUIAutomationGridPattern::GetItem","uiauto.uiauto_IUIAutomationGridPattern_GetItem","uiauto_IUIAutomationGridPattern_GetItem","uiautomationclient/IUIAutomationGridPattern::GetItem","winauto.uiauto_IUIAutomationGridPattern_GetItem"]
old-location: winauto\uiauto_IUIAutomationGridPattern_GetItem.htm
tech.root: WinAuto
ms.assetid: e18fd4ba-7fe2-4acb-97cd-c446d359dc38
ms.date: 12/05/2018
ms.keywords: GetItem, GetItem method [Windows Accessibility], GetItem method [Windows Accessibility],IUIAutomationGridPattern interface, IUIAutomationGridPattern interface [Windows Accessibility],GetItem method, IUIAutomationGridPattern.GetItem, IUIAutomationGridPattern::GetItem, uiauto.uiauto_IUIAutomationGridPattern_GetItem, uiauto_IUIAutomationGridPattern_GetItem, uiautomationclient/IUIAutomationGridPattern::GetItem, winauto.uiauto_IUIAutomationGridPattern_GetItem
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
 - IUIAutomationGridPattern::GetItem
 - uiautomationclient/IUIAutomationGridPattern::GetItem
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
 - IUIAutomationGridPattern.GetItem
---

# IUIAutomationGridPattern::GetItem


## -description

Retrieves a UI Automation element representing an item in the grid.

## -parameters

### -param row [in]

Type: <b>int</b>

The zero-based index of the row.

### -param column [in]

Type: <b>int</b>

The zero-based index of the column.

### -param element [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>**</b>

Receives a pointer to the element representing the grid item.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationgridpattern">IUIAutomationGridPattern</a>