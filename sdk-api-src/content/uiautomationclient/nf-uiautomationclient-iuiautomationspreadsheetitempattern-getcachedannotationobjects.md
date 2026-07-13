---
UID: NF:uiautomationclient.IUIAutomationSpreadsheetItemPattern.GetCachedAnnotationObjects
title: IUIAutomationSpreadsheetItemPattern::GetCachedAnnotationObjects (uiautomationclient.h)
description: Retrieves a cached array of elements representing the annotations associated with this spreadsheet cell.
helpviewer_keywords: ["GetCachedAnnotationObjects","GetCachedAnnotationObjects method [Windows Accessibility]","GetCachedAnnotationObjects method [Windows Accessibility]","IUIAutomationSpreadsheetItemPattern interface","IUIAutomationSpreadsheetItemPattern interface [Windows Accessibility]","GetCachedAnnotationObjects method","IUIAutomationSpreadsheetItemPattern.GetCachedAnnotationObjects","IUIAutomationSpreadsheetItemPattern::GetCachedAnnotationObjects","uiautomationclient/IUIAutomationSpreadsheetItemPattern::GetCachedAnnotationObjects","winauto.uiauto_IUIAutomationSpreadsheetItemPattern_GetCachedAnnotationObjects"]
old-location: winauto\uiauto_IUIAutomationSpreadsheetItemPattern_GetCachedAnnotationObjects.htm
tech.root: WinAuto
ms.assetid: C2F11DD7-60D0-4848-98DD-FC33FD51BBD4
ms.date: 12/05/2018
ms.keywords: GetCachedAnnotationObjects, GetCachedAnnotationObjects method [Windows Accessibility], GetCachedAnnotationObjects method [Windows Accessibility],IUIAutomationSpreadsheetItemPattern interface, IUIAutomationSpreadsheetItemPattern interface [Windows Accessibility],GetCachedAnnotationObjects method, IUIAutomationSpreadsheetItemPattern.GetCachedAnnotationObjects, IUIAutomationSpreadsheetItemPattern::GetCachedAnnotationObjects, uiautomationclient/IUIAutomationSpreadsheetItemPattern::GetCachedAnnotationObjects, winauto.uiauto_IUIAutomationSpreadsheetItemPattern_GetCachedAnnotationObjects
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
 - IUIAutomationSpreadsheetItemPattern::GetCachedAnnotationObjects
 - uiautomationclient/IUIAutomationSpreadsheetItemPattern::GetCachedAnnotationObjects
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
 - IUIAutomationSpreadsheetItemPattern.GetCachedAnnotationObjects
---

# IUIAutomationSpreadsheetItemPattern::GetCachedAnnotationObjects


## -description

Retrieves a cached array of elements representing the annotations associated with this spreadsheet cell.

## -parameters

### -param retVal [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelementarray">IUIAutomationElementArray</a>**</b>

Receives the cached array of annotation elements for this spreadsheet cell.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern">IUIAutomationSpreadsheetItemPattern</a>