---
UID: NF:uiautomationcoreapi.UiaProviderFromIAccessible
title: UiaProviderFromIAccessible function (uiautomationcoreapi.h)
description: Creates a Microsoft UI Automation provider based on the specified Microsoft Active Accessibility object.
helpviewer_keywords: ["UIA_PFIA_DEFAULT","UIA_PFIA_UNWRAP_BRIDGE","UiaProviderFromIAccessible","UiaProviderFromIAccessible function [Windows Accessibility]","uiautomationcoreapi/UiaProviderFromIAccessible","winauto.uiauto_UiaProviderFromIAccessibleFunction"]
old-location: winauto\uiauto_UiaProviderFromIAccessibleFunction.htm
tech.root: WinAuto
ms.assetid: 9858B3B2-CE93-4209-BAFE-BFC911042800
ms.date: 12/05/2018
ms.keywords: UIA_PFIA_DEFAULT, UIA_PFIA_UNWRAP_BRIDGE, UiaProviderFromIAccessible, UiaProviderFromIAccessible function [Windows Accessibility], uiautomationcoreapi/UiaProviderFromIAccessible, winauto.uiauto_UiaProviderFromIAccessibleFunction
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UiaProviderFromIAccessible
 - uiautomationcoreapi/UiaProviderFromIAccessible
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - UiaProviderFromIAccessible
---

# UiaProviderFromIAccessible function


## -description

Creates a Microsoft UI Automation provider based on the specified Microsoft Active Accessibility object.

## -parameters

### -param pAccessible [in]

Type: <b><a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>*</b>

A pointer to the Microsoft Active Accessibility object.

### -param idChild [in]

Type: <b>long</b>

The child ID of the Microsoft Active Accessibility object.

### -param dwFlags [in]

Type: <b>DWORD</b>


One of the following values:



<a id="UIA_PFIA_DEFAULT"></a>
<a id="uia_pfia_default"></a>


#### UIA_PFIA_DEFAULT

<a id="UIA_PFIA_UNWRAP_BRIDGE"></a>
<a id="uia_pfia_unwrap_bridge"></a>


#### UIA_PFIA_UNWRAP_BRIDGE

### -param ppProvider [out]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>**</b>

The new UI Automation provider.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

UI Automation provides backward compatibility for Microsoft Active Accessibility providers by supplying a proxy for them, called the Microsoft Active Accessibility to UI Automation proxy.  This proxy is created automatically when a window responds to a [WM_GETOBJECT](/windows/win32/winauto/wm-getobject) message by returning a Microsoft Active Accessibility provider.  Use <b>UiaProviderFromIAccessible</b> when you need to create a Microsoft Active Accessibility to UI Automation proxy manually; for example, when implementing the <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iaccessibleex">IAccessibleEx</a> interface.  

Some properties, such as LabeledBy, must be expressed as a UI Automation provider.  An <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iaccessibleex">IAccessibleEx</a> provider can use <b>UiaProviderFromIAccessible</b> to wrap an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> object to return it as the value of the LabeledBy property.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-functions">Functions for Providers</a>



<a href="/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaiaccessiblefromprovider">UiaIAccessibleFromProvider</a>