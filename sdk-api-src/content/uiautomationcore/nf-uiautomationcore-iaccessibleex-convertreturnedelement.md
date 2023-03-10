---
UID: NF:uiautomationcore.IAccessibleEx.ConvertReturnedElement
title: IAccessibleEx::ConvertReturnedElement (uiautomationcore.h)
description: Retrieves the IAccessibleEx interface of an element returned as a property value.
helpviewer_keywords: ["ConvertReturnedElement","ConvertReturnedElement method [Windows Accessibility]","ConvertReturnedElement method [Windows Accessibility]","IAccessibleEx interface","IAccessibleEx interface [Windows Accessibility]","ConvertReturnedElement method","IAccessibleEx.ConvertReturnedElement","IAccessibleEx::ConvertReturnedElement","uiauto.uiauto_IAccessibleEx_ConvertReturnedElement","uiauto_IAccessibleEx_ConvertReturnedElement","uiautomationcore/IAccessibleEx::ConvertReturnedElement","winauto.uiauto_IAccessibleEx_ConvertReturnedElement"]
old-location: winauto\uiauto_IAccessibleEx_ConvertReturnedElement.htm
tech.root: WinAuto
ms.assetid: eafda7ed-b18c-4d52-9d1c-a9d1a2d5dfd1
ms.date: 12/05/2018
ms.keywords: ConvertReturnedElement, ConvertReturnedElement method [Windows Accessibility], ConvertReturnedElement method [Windows Accessibility],IAccessibleEx interface, IAccessibleEx interface [Windows Accessibility],ConvertReturnedElement method, IAccessibleEx.ConvertReturnedElement, IAccessibleEx::ConvertReturnedElement, uiauto.uiauto_IAccessibleEx_ConvertReturnedElement, uiauto_IAccessibleEx_ConvertReturnedElement, uiautomationcore/IAccessibleEx::ConvertReturnedElement, winauto.uiauto_IAccessibleEx_ConvertReturnedElement
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - IAccessibleEx::ConvertReturnedElement
 - uiautomationcore/IAccessibleEx::ConvertReturnedElement
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
 - IAccessibleEx.ConvertReturnedElement
---

# IAccessibleEx::ConvertReturnedElement


## -description

Retrieves the <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iaccessibleex">IAccessibleEx</a> interface of an element returned as a property value.

## -parameters

### -param pIn [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>*</b>

Pointer to the <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a> interface that was retrieved as a property.

### -param ppRetValOut [out]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iaccessibleex">IAccessibleEx</a>**</b>

Receives a pointer to the <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iaccessibleex">IAccessibleEx</a>  interface of the element.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is implemented by the bridge between Microsoft UI Automation and Microsoft Active Accessibility. Most other implementations should return E_NOTIMPL after setting <i>ppRetValOut</i> to <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iaccessibleex">IAccessibleEx</a>