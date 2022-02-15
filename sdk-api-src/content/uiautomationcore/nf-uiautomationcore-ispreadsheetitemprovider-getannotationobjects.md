---
UID: NF:uiautomationcore.ISpreadsheetItemProvider.GetAnnotationObjects
title: ISpreadsheetItemProvider::GetAnnotationObjects (uiautomationcore.h)
description: Retrieves an array of objects that represent the annotations associated with this spreadsheet cell.
helpviewer_keywords: ["GetAnnotationObjects","GetAnnotationObjects method [Windows Accessibility]","GetAnnotationObjects method [Windows Accessibility]","ISpreadsheetItemProvider interface","ISpreadsheetItemProvider interface [Windows Accessibility]","GetAnnotationObjects method","ISpreadsheetItemProvider.GetAnnotationObjects","ISpreadsheetItemProvider::GetAnnotationObjects","uiautomationcore/ISpreadsheetItemProvider::GetAnnotationObjects","winauto.uiauto_ISpreadsheetItemProvider_GetAnnotationObjects"]
old-location: winauto\uiauto_ISpreadsheetItemProvider_GetAnnotationObjects.htm
tech.root: WinAuto
ms.assetid: 5B9BDAF8-A7A7-492B-97F7-8502E630203F
ms.date: 12/05/2018
ms.keywords: GetAnnotationObjects, GetAnnotationObjects method [Windows Accessibility], GetAnnotationObjects method [Windows Accessibility],ISpreadsheetItemProvider interface, ISpreadsheetItemProvider interface [Windows Accessibility],GetAnnotationObjects method, ISpreadsheetItemProvider.GetAnnotationObjects, ISpreadsheetItemProvider::GetAnnotationObjects, uiautomationcore/ISpreadsheetItemProvider::GetAnnotationObjects, winauto.uiauto_ISpreadsheetItemProvider_GetAnnotationObjects
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
 - ISpreadsheetItemProvider::GetAnnotationObjects
 - uiautomationcore/ISpreadsheetItemProvider::GetAnnotationObjects
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
 - ISpreadsheetItemProvider.GetAnnotationObjects
---

# ISpreadsheetItemProvider::GetAnnotationObjects


## -description

Retrieves an array of objects that represent the annotations associated with this spreadsheet cell.

## -parameters

### -param pRetVal [out, retval]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>**</b>

Receives an array of <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a> interfaces that represent the annotations associated with the spreadsheet cell.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetitemprovider">ISpreadsheetItemProvider</a>