---
UID: NF:uiautomationcoreapi.UiaIAccessibleFromProvider
title: UiaIAccessibleFromProvider function (uiautomationcoreapi.h)
description: Retrieves an IAccessible implementation that provides Microsoft Active Accessibility data on behalf of a Microsoft UI Automation provider.
helpviewer_keywords: ["UIA_IAFP_DEFAULT","UIA_IAFP_UNWRAP_BRIDGE","UiaIAccessibleFromProvider","UiaIAccessibleFromProvider function [Windows Accessibility]","uiautomationcoreapi/UiaIAccessibleFromProvider","winauto.uiauto_UiaIAccessibleFromProvider"]
old-location: winauto\uiauto_UiaIAccessibleFromProvider.htm
tech.root: WinAuto
ms.assetid: 79523637-9858-4E0B-87E7-8CED19FADF0E
ms.date: 12/05/2018
ms.keywords: UIA_IAFP_DEFAULT, UIA_IAFP_UNWRAP_BRIDGE, UiaIAccessibleFromProvider, UiaIAccessibleFromProvider function [Windows Accessibility], uiautomationcoreapi/UiaIAccessibleFromProvider, winauto.uiauto_UiaIAccessibleFromProvider
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - UiaIAccessibleFromProvider
 - uiautomationcoreapi/UiaIAccessibleFromProvider
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
 - UiaIAccessibleFromProvider
---

# UiaIAccessibleFromProvider function


## -description

Retrieves an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> implementation that provides Microsoft Active Accessibility data on behalf of a Microsoft UI Automation provider.

## -parameters

### -param pProvider [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>*</b>

A pointer to the UI Automation object.

### -param dwFlags [in]

Type: <b>DWORD</b>


One of the following values:



<a id="UIA_IAFP_DEFAULT"></a>
<a id="uia_iafp_default"></a>


#### UIA_IAFP_DEFAULT

<a id="UIA_IAFP_UNWRAP_BRIDGE"></a>
<a id="uia_iafp_unwrap_bridge"></a>


#### UIA_IAFP_UNWRAP_BRIDGE

### -param ppAccessible [out]

Type: <b><a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>**</b>

Receives the pointer to the <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> implementation for the provider.

### -param pvarChild [out]

Type: <b><a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a>*</b>

Receives the child identifier of the accessible element in the <b>lVal</b> member.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

In most cases, this function retrieves a wrapper object, provided by Windows, that implements <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> on behalf of the <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a> object.  If the provided <b>IRawElementProviderSimple</b> pointer is itself a wrapper object, this function retrieves the wrapped <b>IAccessible</b> pointer and returns that instead, to prevent the creation of multiple layers of wrappers.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-functions">Functions for Providers</a>



<a href="/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaproviderfromiaccessible">UiaProviderFromIAccessible</a>