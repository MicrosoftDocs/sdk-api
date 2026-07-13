---
UID: NF:uiautomationcore.ISpreadsheetProvider.GetItemByName
title: ISpreadsheetProvider::GetItemByName (uiautomationcore.h)
description: Exposes a UI Automation element that represents the spreadsheet cell that has the specified name.
helpviewer_keywords: ["GetItemByName","GetItemByName method [Windows Accessibility]","GetItemByName method [Windows Accessibility]","ISpreadsheetProvider interface","ISpreadsheetProvider interface [Windows Accessibility]","GetItemByName method","ISpreadsheetProvider.GetItemByName","ISpreadsheetProvider::GetItemByName","uiautomationcore/ISpreadsheetProvider::GetItemByName","winauto.uiauto_ISpreadsheetProvider_GetItemByName"]
old-location: winauto\uiauto_ISpreadsheetProvider_GetItemByName.htm
tech.root: WinAuto
ms.assetid: 9A496B3F-5095-4094-BAF6-D4EE20498D4B
ms.date: 12/05/2018
ms.keywords: GetItemByName, GetItemByName method [Windows Accessibility], GetItemByName method [Windows Accessibility],ISpreadsheetProvider interface, ISpreadsheetProvider interface [Windows Accessibility],GetItemByName method, ISpreadsheetProvider.GetItemByName, ISpreadsheetProvider::GetItemByName, uiautomationcore/ISpreadsheetProvider::GetItemByName, winauto.uiauto_ISpreadsheetProvider_GetItemByName
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
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
 - ISpreadsheetProvider::GetItemByName
 - uiautomationcore/ISpreadsheetProvider::GetItemByName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - ISpreadsheetProvider.GetItemByName
---

# ISpreadsheetProvider::GetItemByName


## -description

Exposes a UI Automation element that represents the spreadsheet cell that has the specified name.

## -parameters

### -param name [in]

Type: <b>LPCWSTR</b>

The name of the target cell.

### -param pRetVal [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>**</b>

Receives the element that represents the target cell.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A spreadsheet cell typically has a name such as “c5” or “a15”.  A name can also apply to a range of cells.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider">ISpreadsheetProvider</a>