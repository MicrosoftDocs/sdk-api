---
UID: NF:uiautomationcore.IRawElementProviderSimple.get_HostRawElementProvider
title: IRawElementProviderSimple::get_HostRawElementProvider (uiautomationcore.h)
description: Specifies the host provider for this element.
helpviewer_keywords: ["HostRawElementProvider property [Windows Accessibility]","HostRawElementProvider property [Windows Accessibility]","IRawElementProviderSimple interface","IRawElementProviderSimple interface [Windows Accessibility]","HostRawElementProvider property","IRawElementProviderSimple.HostRawElementProvider","IRawElementProviderSimple.get_HostRawElementProvider","IRawElementProviderSimple::HostRawElementProvider","IRawElementProviderSimple::get_HostRawElementProvider","get_HostRawElementProvider","uiauto.uiauto_IRawElementProviderSimple_HostRawElementProvider","uiauto_IRawElementProviderSimple_HostRawElementProvider","uiautomationcore/IRawElementProviderSimple::HostRawElementProvider","uiautomationcore/IRawElementProviderSimple::get_HostRawElementProvider","winauto.uiauto_IRawElementProviderSimple_HostRawElementProvider"]
old-location: winauto\uiauto_IRawElementProviderSimple_HostRawElementProvider.htm
tech.root: WinAuto
ms.assetid: fcbd3dc8-5bc7-48ae-bc21-009876b3e673
ms.date: 12/05/2018
ms.keywords: HostRawElementProvider property [Windows Accessibility], HostRawElementProvider property [Windows Accessibility],IRawElementProviderSimple interface, IRawElementProviderSimple interface [Windows Accessibility],HostRawElementProvider property, IRawElementProviderSimple.HostRawElementProvider, IRawElementProviderSimple.get_HostRawElementProvider, IRawElementProviderSimple::HostRawElementProvider, IRawElementProviderSimple::get_HostRawElementProvider, get_HostRawElementProvider, uiauto.uiauto_IRawElementProviderSimple_HostRawElementProvider, uiauto_IRawElementProviderSimple_HostRawElementProvider, uiautomationcore/IRawElementProviderSimple::HostRawElementProvider, uiautomationcore/IRawElementProviderSimple::get_HostRawElementProvider, winauto.uiauto_IRawElementProviderSimple_HostRawElementProvider
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - IRawElementProviderSimple::get_HostRawElementProvider
 - uiautomationcore/IRawElementProviderSimple::get_HostRawElementProvider
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
 - IRawElementProviderSimple.HostRawElementProvider
 - IRawElementProviderSimple.get_HostRawElementProvider
---

# IRawElementProviderSimple::get_HostRawElementProvider


## -description

Specifies the host provider for this element.

This property is read-only.

## -parameters

## -remarks

This property is generally the Microsoft UI Automation provider for the window of a custom control.
			UI Automation uses this provider in combination with the custom provider. For example, the runtime identifier 
			of the element is usually obtained from the host provider.

A host provider must be returned in the following cases: when the element is a fragment root, 
			when the element is a simple element (such as a push button), and when the provider is a repositioning placeholder (for more information, see <a href="/windows/desktop/WinAuto/uiauto-serversideprovider">Provider Repositioning</a>). 
			 In other cases, the property should be <b>NULL</b>.


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

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>



<a href="/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiahostproviderfromhwnd">UiaHostProviderFromHwnd</a>