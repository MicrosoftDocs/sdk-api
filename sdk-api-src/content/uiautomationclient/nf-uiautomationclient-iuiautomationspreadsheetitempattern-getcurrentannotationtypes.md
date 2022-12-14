---
UID: NF:uiautomationclient.IUIAutomationSpreadsheetItemPattern.GetCurrentAnnotationTypes
title: IUIAutomationSpreadsheetItemPattern::GetCurrentAnnotationTypes (uiautomationclient.h)
description: Retrieves an array of annotation type identifiers indicating the types of annotations that are associated with this spreadsheet cell. (IUIAutomationSpreadsheetItemPattern.GetCurrentAnnotationTypes)
helpviewer_keywords: ["GetCurrentAnnotationTypes","GetCurrentAnnotationTypes method [Windows Accessibility]","GetCurrentAnnotationTypes method [Windows Accessibility]","IUIAutomationSpreadsheetItemPattern interface","IUIAutomationSpreadsheetItemPattern interface [Windows Accessibility]","GetCurrentAnnotationTypes method","IUIAutomationSpreadsheetItemPattern.GetCurrentAnnotationTypes","IUIAutomationSpreadsheetItemPattern::GetCurrentAnnotationTypes","uiautomationclient/IUIAutomationSpreadsheetItemPattern::GetCurrentAnnotationTypes","winauto.uiauto_IUIAutomationSpreadsheetItemPattern_GetCurrentAnnotationTypes"]
old-location: winauto\uiauto_IUIAutomationSpreadsheetItemPattern_GetCurrentAnnotationTypes.htm
tech.root: WinAuto
ms.assetid: 779CFE43-8127-4A78-BD1A-8407DA5F49A2
ms.date: 12/05/2018
ms.keywords: GetCurrentAnnotationTypes, GetCurrentAnnotationTypes method [Windows Accessibility], GetCurrentAnnotationTypes method [Windows Accessibility],IUIAutomationSpreadsheetItemPattern interface, IUIAutomationSpreadsheetItemPattern interface [Windows Accessibility],GetCurrentAnnotationTypes method, IUIAutomationSpreadsheetItemPattern.GetCurrentAnnotationTypes, IUIAutomationSpreadsheetItemPattern::GetCurrentAnnotationTypes, uiautomationclient/IUIAutomationSpreadsheetItemPattern::GetCurrentAnnotationTypes, winauto.uiauto_IUIAutomationSpreadsheetItemPattern_GetCurrentAnnotationTypes
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
 - IUIAutomationSpreadsheetItemPattern::GetCurrentAnnotationTypes
 - uiautomationclient/IUIAutomationSpreadsheetItemPattern::GetCurrentAnnotationTypes
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
 - IUIAutomationSpreadsheetItemPattern.GetCurrentAnnotationTypes
---

# IUIAutomationSpreadsheetItemPattern::GetCurrentAnnotationTypes


## -description

Retrieves an array of annotation type identifiers indicating the types of annotations that are associated with this spreadsheet cell.

## -parameters

### -param retVal [out, retval]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>**</b>

Receives the array of annotation type identifiers. For a list of possible values, see <a href="/windows/desktop/WinAuto/uiauto-annotation-type-identifiers">Annotation Type Identifiers</a>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern">IUIAutomationSpreadsheetItemPattern</a>
