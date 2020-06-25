---
UID: NN:webauthenticationcoremanagerinterop.IWebAuthenticationCoreManagerInterop
title: IWebAuthenticationCoreManagerInterop
description: Contains core methods for obtaining tokens from web account providers.
helpviewer_keywords: ["IWebAuthenticationCoreManagerInterop"]
ms.date: 5/28/2019
ms.keywords: IWebAuthenticationCoreManagerInterop
f1_keywords:
- webauthenticationcoremanagerinterop/IWebAuthenticationCoreManagerInterop
dev_langs:
- c++
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
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.unicode-ansi: 
topic_type:
- apiref
api_type:
- COM
api_location:
- webauthenticationcoremanagerinterop.h
api_name:
- IWebAuthenticationCoreManagerInterop
tech.root: winrt
---

## -inheritance

## -description

Provides Win32 apps with access to certain functions of [WebAuthenticationCoreManager](/uwp/api/windows.security.authentication.web.core.webauthenticationcoremanager)
that are otherwise available only to UWP apps.

## -remarks

This interface is implemented by WebAuthenticationCoreManager's [activation factory](../activation/nn-activation-iactivationfactory).
To get an object of this interface, get a reference to the activation factory
and then call [IUnknown::QueryInterface](../unknwn/nf-unknwn-iunknown-queryinterface%28refiid_void%29)
on it:

```cppwinrt
using winrt::Windows::Security::Authentication::Web::Core::WebAuthenticationCoreManager;

auto managerFactory = winrt::get_activation_factory<WebAuthenticationCoreManager>();
winrt::com_ptr<IWebAuthenticationCoreManagerInterop> managerInterop{ managerFactory.as<IWebAuthenticationCoreManagerInterop>() };

managerInterop->RequestTokenForWindowAsync(/* ... */)
```


## -see-also