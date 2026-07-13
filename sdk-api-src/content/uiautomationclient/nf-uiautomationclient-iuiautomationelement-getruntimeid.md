---
UID: NF:uiautomationclient.IUIAutomationElement.GetRuntimeId
title: IUIAutomationElement::GetRuntimeId (uiautomationclient.h)
description: Retrieves the unique identifier assigned to the UI element.
helpviewer_keywords: ["GetRuntimeId","GetRuntimeId method [Windows Accessibility]","GetRuntimeId method [Windows Accessibility]","IUIAutomationElement interface","IUIAutomationElement interface [Windows Accessibility]","GetRuntimeId method","IUIAutomationElement.GetRuntimeId","IUIAutomationElement::GetRuntimeId","uiauto.uiauto_IUIAutomationElement_GetRuntimeId","uiauto_IUIAutomationElement_GetRuntimeId","uiautomationclient/IUIAutomationElement::GetRuntimeId","winauto.uiauto_IUIAutomationElement_GetRuntimeId"]
old-location: winauto\uiauto_IUIAutomationElement_GetRuntimeId.htm
tech.root: WinAuto
ms.assetid: d351f2ca-d9de-4055-8356-9a100a77f397
ms.date: 12/05/2018
ms.keywords: GetRuntimeId, GetRuntimeId method [Windows Accessibility], GetRuntimeId method [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],GetRuntimeId method, IUIAutomationElement.GetRuntimeId, IUIAutomationElement::GetRuntimeId, uiauto.uiauto_IUIAutomationElement_GetRuntimeId, uiauto_IUIAutomationElement_GetRuntimeId, uiautomationclient/IUIAutomationElement::GetRuntimeId, winauto.uiauto_IUIAutomationElement_GetRuntimeId
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
 - IUIAutomationElement::GetRuntimeId
 - uiautomationclient/IUIAutomationElement::GetRuntimeId
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
 - IUIAutomationElement.GetRuntimeId
---

# IUIAutomationElement::GetRuntimeId


## -description

Retrieves the unique identifier assigned to the UI element.

## -parameters

### -param runtimeId [out, retval]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>**</b>

Receives a pointer to the runtime ID as an array of integers.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The identifier is only guaranteed to be unique to the UI of the desktop on which it was generated. Identifiers can be reused over time.

The format of run-time identifiers might change in the future. The returned identifier should be treated as an opaque value and used only for comparison; for example, to determine whether a Microsoft UI Automation element is in the cache.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-automation-element-propids">Automation Element Property IDs</a>



<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-compareruntimeids">CompareRuntimeIds</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>



<b>Reference</b>