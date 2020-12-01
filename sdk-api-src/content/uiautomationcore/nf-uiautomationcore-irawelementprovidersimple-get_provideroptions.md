---
UID: NF:uiautomationcore.IRawElementProviderSimple.get_ProviderOptions
title: IRawElementProviderSimple::get_ProviderOptions (uiautomationcore.h)
description: Specifies the type of Microsoft UI Automation provider; for example, whether it is a client-side (proxy) or server-side provider.
helpviewer_keywords: ["IRawElementProviderSimple interface [Windows Accessibility]","ProviderOptions property","IRawElementProviderSimple.ProviderOptions","IRawElementProviderSimple.get_ProviderOptions","IRawElementProviderSimple::ProviderOptions","IRawElementProviderSimple::get_ProviderOptions","ProviderOptions property [Windows Accessibility]","ProviderOptions property [Windows Accessibility]","IRawElementProviderSimple interface","get_ProviderOptions","uiauto.uiauto_IRawElementProviderSimple_ProviderOptions","uiauto_IRawElementProviderSimple_ProviderOptions","uiautomationcore/IRawElementProviderSimple::ProviderOptions","uiautomationcore/IRawElementProviderSimple::get_ProviderOptions","winauto.uiauto_IRawElementProviderSimple_ProviderOptions"]
old-location: winauto\uiauto_IRawElementProviderSimple_ProviderOptions.htm
tech.root: WinAuto
ms.assetid: fd41bb43-bbf1-4022-9472-0ad2816074c6
ms.date: 12/05/2018
ms.keywords: IRawElementProviderSimple interface [Windows Accessibility],ProviderOptions property, IRawElementProviderSimple.ProviderOptions, IRawElementProviderSimple.get_ProviderOptions, IRawElementProviderSimple::ProviderOptions, IRawElementProviderSimple::get_ProviderOptions, ProviderOptions property [Windows Accessibility], ProviderOptions property [Windows Accessibility],IRawElementProviderSimple interface, get_ProviderOptions, uiauto.uiauto_IRawElementProviderSimple_ProviderOptions, uiauto_IRawElementProviderSimple_ProviderOptions, uiautomationcore/IRawElementProviderSimple::ProviderOptions, uiautomationcore/IRawElementProviderSimple::get_ProviderOptions, winauto.uiauto_IRawElementProviderSimple_ProviderOptions
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
 - IRawElementProviderSimple::get_ProviderOptions
 - uiautomationcore/IRawElementProviderSimple::get_ProviderOptions
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
 - IRawElementProviderSimple.ProviderOptions
 - IRawElementProviderSimple.get_ProviderOptions
---

# IRawElementProviderSimple::get_ProviderOptions


## -description

Specifies the type of Microsoft UI Automation provider; for example, whether it is a client-side (proxy) or server-side provider.

This property is read-only.

## -parameters

## -remarks

The method must return either <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-provideroptions">ProviderOptions_ServerSideProvider</a> or <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-provideroptions">ProviderOptions_ClientSideProvider</a>.

UI Automation handles the various types of providers differently. 
			For example, events from a server-side provider are broadcast to all listening clients, 
			but events from client-side (proxy) providers remain in the client.


#### Examples

The following example implements this method for a server-side UI Automation provider.
			


```cpp
HRESULT STDMETHODCALLTYPE Provider::get_ProviderOptions( ProviderOptions* pRetVal )
{
    *pRetVal = ProviderOptions_ServerSideProvider;
    return S_OK;
}    
```

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>