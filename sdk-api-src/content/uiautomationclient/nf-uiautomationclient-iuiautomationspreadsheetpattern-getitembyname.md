---
UID: NF:uiautomationclient.IUIAutomationSpreadsheetPattern.GetItemByName
title: IUIAutomationSpreadsheetPattern::GetItemByName (uiautomationclient.h)
description: Retrieves a UI Automation element that represents the spreadsheet cell that has the specified name.
helpviewer_keywords: ["GetItemByName","GetItemByName method [Windows Accessibility]","GetItemByName method [Windows Accessibility]","IUIAutomationSpreadsheetPattern interface","IUIAutomationSpreadsheetPattern interface [Windows Accessibility]","GetItemByName method","IUIAutomationSpreadsheetPattern.GetItemByName","IUIAutomationSpreadsheetPattern::GetItemByName","uiautomationclient/IUIAutomationSpreadsheetPattern::GetItemByName","winauto.uiauto_IUIAutomationSpreadsheetPattern_GetItemByName"]
old-location: winauto\uiauto_IUIAutomationSpreadsheetPattern_GetItemByName.htm
tech.root: WinAuto
ms.assetid: 4CDE57FA-1B94-408E-B1E6-3CD3CFC5AB82
ms.date: 12/05/2018
ms.keywords: GetItemByName, GetItemByName method [Windows Accessibility], GetItemByName method [Windows Accessibility],IUIAutomationSpreadsheetPattern interface, IUIAutomationSpreadsheetPattern interface [Windows Accessibility],GetItemByName method, IUIAutomationSpreadsheetPattern.GetItemByName, IUIAutomationSpreadsheetPattern::GetItemByName, uiautomationclient/IUIAutomationSpreadsheetPattern::GetItemByName, winauto.uiauto_IUIAutomationSpreadsheetPattern_GetItemByName
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
 - IUIAutomationSpreadsheetPattern::GetItemByName
 - uiautomationclient/IUIAutomationSpreadsheetPattern::GetItemByName
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
 - IUIAutomationSpreadsheetPattern.GetItemByName
---

# IUIAutomationSpreadsheetPattern::GetItemByName


## -description

Retrieves a UI Automation element that represents the spreadsheet cell that has the specified name.

## -parameters

### -param name [in]

Type: <b>BSTR</b>

The name of the target cell.

### -param element [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>**</b>

Receives the element that represents the target cell.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetpattern">IUIAutomationSpreadsheetPattern</a>