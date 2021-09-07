---
UID: NF:uiautomationclient.IUIAutomationLegacyIAccessiblePattern.GetIAccessible
title: IUIAutomationLegacyIAccessiblePattern::GetIAccessible (uiautomationclient.h)
description: Retrieves an IAccessible object that corresponds to the Microsoft UI Automation element.
helpviewer_keywords: ["GetIAccessible","GetIAccessible method [Windows Accessibility]","GetIAccessible method [Windows Accessibility]","IUIAutomationLegacyIAccessiblePattern interface","IUIAutomationLegacyIAccessiblePattern interface [Windows Accessibility]","GetIAccessible method","IUIAutomationLegacyIAccessiblePattern.GetIAccessible","IUIAutomationLegacyIAccessiblePattern::GetIAccessible","uiauto.uiauto_IUIAutomationLegacyIAccessiblePattern_GetIAccessible","uiauto_IUIAutomationLegacyIAccessiblePattern_GetIAccessible","uiautomationclient/IUIAutomationLegacyIAccessiblePattern::GetIAccessible","winauto.uiauto_IUIAutomationLegacyIAccessiblePattern_GetIAccessible"]
old-location: winauto\uiauto_IUIAutomationLegacyIAccessiblePattern_GetIAccessible.htm
tech.root: WinAuto
ms.assetid: 58ce3005-dfac-4ffe-b874-69a2f994e7a6
ms.date: 12/05/2018
ms.keywords: GetIAccessible, GetIAccessible method [Windows Accessibility], GetIAccessible method [Windows Accessibility],IUIAutomationLegacyIAccessiblePattern interface, IUIAutomationLegacyIAccessiblePattern interface [Windows Accessibility],GetIAccessible method, IUIAutomationLegacyIAccessiblePattern.GetIAccessible, IUIAutomationLegacyIAccessiblePattern::GetIAccessible, uiauto.uiauto_IUIAutomationLegacyIAccessiblePattern_GetIAccessible, uiauto_IUIAutomationLegacyIAccessiblePattern_GetIAccessible, uiautomationclient/IUIAutomationLegacyIAccessiblePattern::GetIAccessible, winauto.uiauto_IUIAutomationLegacyIAccessiblePattern_GetIAccessible
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IUIAutomationLegacyIAccessiblePattern::GetIAccessible
 - uiautomationclient/IUIAutomationLegacyIAccessiblePattern::GetIAccessible
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
 - IUIAutomationLegacyIAccessiblePattern.GetIAccessible
---

# IUIAutomationLegacyIAccessiblePattern::GetIAccessible


## -description

Retrieves an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> object that corresponds to the Microsoft UI Automation element.

## -parameters

### -param ppAccessible [out, retval]

Type: <b><a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>**</b>

Receives a pointer to an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface for the accessible object.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method returns <b>NULL</b> if the underlying implementation of the UI Automation element is not a native Microsoft Active Accessibility server; that is, if a client attempts to retrieve the <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface for an element originally supported by a proxy object from OLEACC.dll, or by the UIA-to-MSAA Bridge.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern">IUIAutomationLegacyIAccessiblePattern</a>