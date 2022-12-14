---
UID: NN:webauthenticationcoremanagerinterop.IWebAuthenticationCoreManagerInterop
title: IWebAuthenticationCoreManagerInterop
description: Contains core methods for obtaining tokens from web account providers.
helpviewer_keywords: ["IWebAuthenticationCoreManagerInterop"]
ms.date: 5/28/2019
ms.keywords: IWebAuthenticationCoreManagerInterop
targetos: Windows
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: webauthenticationcoremanagerinterop.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.unicode-ansi: 
tech.root: winrt
f1_keywords:
 - IWebAuthenticationCoreManagerInterop
 - webauthenticationcoremanagerinterop/IWebAuthenticationCoreManagerInterop
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - webauthenticationcoremanagerinterop.h
api_name:
 - IWebAuthenticationCoreManagerInterop
---

## -description

Provides Win32 apps with access to certain functions of [WebAuthenticationCoreManager](/uwp/api/windows.security.authentication.web.core.webauthenticationcoremanager)
that are otherwise available only to UWP apps.

## -inheritance

## -remarks

This interface is implemented by WebAuthenticationCoreManager's [activation factory](../activation/nn-activation-iactivationfactory.md).
To get an object of this interface, get a reference to the activation factory
and then call [IUnknown::QueryInterface](../unknwn/nf-unknwn-iunknown-queryinterface%28refiid_void%29.md)
on it:

```cppwinrt
using winrt::Windows::Security::Authentication::Web::Core::WebAuthenticationCoreManager;

auto managerFactory = winrt::get_activation_factory<WebAuthenticationCoreManager>();
winrt::com_ptr<IWebAuthenticationCoreManagerInterop> managerInterop{ managerFactory.as<IWebAuthenticationCoreManagerInterop>() };

managerInterop->RequestTokenForWindowAsync(/* ... */)
```

## -see-also

