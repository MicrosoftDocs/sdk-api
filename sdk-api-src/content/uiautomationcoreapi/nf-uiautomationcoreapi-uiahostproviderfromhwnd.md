---
UID: NF:uiautomationcoreapi.UiaHostProviderFromHwnd
title: UiaHostProviderFromHwnd function (uiautomationcoreapi.h)
description: Gets the host provider for a window.
helpviewer_keywords: ["UiaHostProviderFromHwnd","UiaHostProviderFromHwnd function [Windows Accessibility]","uiauto.uiauto_UiaHostProviderFromHwndFunction","uiauto_UiaHostProviderFromHwndFunction","uiautomationcoreapi/UiaHostProviderFromHwnd","winauto.uiauto_UiaHostProviderFromHwndFunction"]
old-location: winauto\uiauto_UiaHostProviderFromHwndFunction.htm
tech.root: WinAuto
ms.assetid: 8cc8a8d8-a4e0-477e-bf3b-2fd5df2b9db1
ms.date: 12/05/2018
ms.keywords: UiaHostProviderFromHwnd, UiaHostProviderFromHwnd function [Windows Accessibility], uiauto.uiauto_UiaHostProviderFromHwndFunction, uiauto_UiaHostProviderFromHwndFunction, uiautomationcoreapi/UiaHostProviderFromHwnd, winauto.uiauto_UiaHostProviderFromHwndFunction
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - UiaHostProviderFromHwnd
 - uiautomationcoreapi/UiaHostProviderFromHwnd
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
 - Ext-MS-Win-uiacore-l1-1-0.dll
 - Ext-MS-Win-UIaCore-l1-1-1.dll
 - Ext-MS-Win-UIaCore-l1-1-2.dll
 - Ext-MS-Win-UiaCore-L1-1-3.dll
api_name:
 - UiaHostProviderFromHwnd
---

# UiaHostProviderFromHwnd function


## -description

Gets the host provider for a window.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The window containing the element served by the provider.

### -param ppProvider [out]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>**</b>

The host provider for the window.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The object retrieved by this function is useful only for responding to calls to the <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider">IRawElementProviderSimple::get_HostRawElementProvider</a> method. You cannot use the object to raise events, provide properties, and so on.  If you need to raise events or provide properties, you must create a provider object that fully implements the <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a> interface.


#### Examples

The following example returns the host provider for the window that hosts the control served by 
            this provider.


```cpp
HRESULT STDMETHODCALLTYPE Provider::get_HostRawElementProvider(IRawElementProviderSimple** pRetVal)
{
    return UiaHostProviderFromHwnd(controlHWnd, pRetVal); 
} 
```

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-functions">Functions for Providers</a>