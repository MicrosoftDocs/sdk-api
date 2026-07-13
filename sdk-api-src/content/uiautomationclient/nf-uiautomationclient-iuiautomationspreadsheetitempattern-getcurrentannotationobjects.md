---
UID: NF:uiautomationclient.IUIAutomationSpreadsheetItemPattern.GetCurrentAnnotationObjects
title: IUIAutomationSpreadsheetItemPattern::GetCurrentAnnotationObjects (uiautomationclient.h)
description: Retrieves an array of elements representing the annotations associated with this spreadsheet cell.
helpviewer_keywords: ["GetCurrentAnnotationObjects","GetCurrentAnnotationObjects method [Windows Accessibility]","GetCurrentAnnotationObjects method [Windows Accessibility]","IUIAutomationSpreadsheetItemPattern interface","IUIAutomationSpreadsheetItemPattern interface [Windows Accessibility]","GetCurrentAnnotationObjects method","IUIAutomationSpreadsheetItemPattern.GetCurrentAnnotationObjects","IUIAutomationSpreadsheetItemPattern::GetCurrentAnnotationObjects","uiautomationclient/IUIAutomationSpreadsheetItemPattern::GetCurrentAnnotationObjects","winauto.uiauto_IUIAutomationSpreadsheetItemPattern_GetCurrentAnnotationObjects"]
old-location: winauto\uiauto_IUIAutomationSpreadsheetItemPattern_GetCurrentAnnotationObjects.htm
tech.root: WinAuto
ms.assetid: 876ED365-C860-4C71-BF98-D940D49F2A9D
ms.date: 12/05/2018
ms.keywords: GetCurrentAnnotationObjects, GetCurrentAnnotationObjects method [Windows Accessibility], GetCurrentAnnotationObjects method [Windows Accessibility],IUIAutomationSpreadsheetItemPattern interface, IUIAutomationSpreadsheetItemPattern interface [Windows Accessibility],GetCurrentAnnotationObjects method, IUIAutomationSpreadsheetItemPattern.GetCurrentAnnotationObjects, IUIAutomationSpreadsheetItemPattern::GetCurrentAnnotationObjects, uiautomationclient/IUIAutomationSpreadsheetItemPattern::GetCurrentAnnotationObjects, winauto.uiauto_IUIAutomationSpreadsheetItemPattern_GetCurrentAnnotationObjects
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
 - IUIAutomationSpreadsheetItemPattern::GetCurrentAnnotationObjects
 - uiautomationclient/IUIAutomationSpreadsheetItemPattern::GetCurrentAnnotationObjects
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
 - IUIAutomationSpreadsheetItemPattern.GetCurrentAnnotationObjects
---

# IUIAutomationSpreadsheetItemPattern::GetCurrentAnnotationObjects


## -description

Retrieves an array of elements representing the annotations associated with this spreadsheet cell.

## -parameters

### -param retVal [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelementarray">IUIAutomationElementArray</a>**</b>

Receives the array of annotation elements for this spreadsheet cell.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern">IUIAutomationSpreadsheetItemPattern</a>