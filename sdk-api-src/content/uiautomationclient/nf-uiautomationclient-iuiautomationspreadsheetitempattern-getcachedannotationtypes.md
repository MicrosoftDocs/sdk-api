---
UID: NF:uiautomationclient.IUIAutomationSpreadsheetItemPattern.GetCachedAnnotationTypes
title: IUIAutomationSpreadsheetItemPattern::GetCachedAnnotationTypes (uiautomationclient.h)
description: Retrieves a cached array of annotation type identifiers indicating the types of annotations that are associated with this spreadsheet cell.
helpviewer_keywords: ["GetCachedAnnotationTypes","GetCachedAnnotationTypes method [Windows Accessibility]","GetCachedAnnotationTypes method [Windows Accessibility]","IUIAutomationSpreadsheetItemPattern interface","IUIAutomationSpreadsheetItemPattern interface [Windows Accessibility]","GetCachedAnnotationTypes method","IUIAutomationSpreadsheetItemPattern.GetCachedAnnotationTypes","IUIAutomationSpreadsheetItemPattern::GetCachedAnnotationTypes","uiautomationclient/IUIAutomationSpreadsheetItemPattern::GetCachedAnnotationTypes","winauto.uiauto_IUIAutomationSpreadsheetItemPattern_GetCachedAnnotationTypes"]
old-location: winauto\uiauto_IUIAutomationSpreadsheetItemPattern_GetCachedAnnotationTypes.htm
tech.root: WinAuto
ms.assetid: CF146EB3-AF26-40C0-A19C-78692EE76E92
ms.date: 12/05/2018
ms.keywords: GetCachedAnnotationTypes, GetCachedAnnotationTypes method [Windows Accessibility], GetCachedAnnotationTypes method [Windows Accessibility],IUIAutomationSpreadsheetItemPattern interface, IUIAutomationSpreadsheetItemPattern interface [Windows Accessibility],GetCachedAnnotationTypes method, IUIAutomationSpreadsheetItemPattern.GetCachedAnnotationTypes, IUIAutomationSpreadsheetItemPattern::GetCachedAnnotationTypes, uiautomationclient/IUIAutomationSpreadsheetItemPattern::GetCachedAnnotationTypes, winauto.uiauto_IUIAutomationSpreadsheetItemPattern_GetCachedAnnotationTypes
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
 - IUIAutomationSpreadsheetItemPattern::GetCachedAnnotationTypes
 - uiautomationclient/IUIAutomationSpreadsheetItemPattern::GetCachedAnnotationTypes
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
 - IUIAutomationSpreadsheetItemPattern.GetCachedAnnotationTypes
---

# IUIAutomationSpreadsheetItemPattern::GetCachedAnnotationTypes


## -description

Retrieves a cached array of annotation type identifiers indicating the types of annotations that are associated with this spreadsheet cell.

## -parameters

### -param retVal [out, retval]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>**</b>

Receives the cached array of annotation type identifiers. For a list of possible values, see <a href="/windows/desktop/WinAuto/uiauto-annotation-type-identifiers">Annotation Type Identifiers</a>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern">IUIAutomationSpreadsheetItemPattern</a>