---
UID: NF:webauthenticationcoremanagerinterop.IWebAuthenticationCoreManagerInterop.RequestTokenForWindowAsync
title: IWebAuthenticationCoreManagerInterop::RequestTokenForWindowAsync
description: Asynchronously requests a token from a web account provider. If necessary, the user is prompted to enter their credentials.helpviewer_keywords: ["IWebAuthenticationCoreManagerInterop::RequestTokenForWindowAsync"]
ms.date: 5/28/2019
ms.keywords: IWebAuthenticationCoreManagerInterop::RequestTokenForWindowAsync
f1_keywords:
- webauthenticationcoremanagerinterop/IWebAuthenticationCoreManagerInterop::RequestTokenForWindowAsync
dev_langs:
- c++
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: webauthenticationcoremanagerinterop.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
- apiref
api_type:
- COM
api_location:
- webauthenticationcoremanagerinterop.h
api_name:
- IWebAuthenticationCoreManagerInterop::RequestTokenForWindowAsync
tech.root: winrt
---

## -description

Asynchronously requests a token from a web account provider. If necessary, the user is prompted to enter their credentials.

## -parameters

### -param appWindow

The window to be used as the parent for the window prompting the user for credentials,
if such a window is necessary.

### -param request

The web token request, given as an instance of the
[WebTokenRequest](/uwp/api/windows.security.authentication.web.core.webtokenrequest)
class type-casted to the [IInspectable](../inspectable/nn-inspectable-iinspectable.md)
interface.

### -param riid

Must refer to the [interface identifier (IID)](https://docs.microsoft.com/openspecs/windows_protocols/ms-oaut/bbde795f-5398-42d8-9f59-3613da03c318)
for the interface
[IAsyncOperation](/uwp/api/windows.foundation.iasyncoperation-1)&lt;[WebTokenRequestResult](/uwp/api/windows.security.authentication.web.core.webtokenrequestresult)&gt;.
This IID is automatically generated but you can obtain it programatically:

```cppwinrt
using winrt::Windows::Foundation::IAsyncOperation;
using winrt::Windows::Security::Authentication::Web::Core::WebTokenRequestResult;

constexpr winrt::guid iidAsyncRequestResult{ winrt::guid_of<IAsyncOperation<WebTokenRequestResult>>() };
```

### -param asyncInfo

The address of a pointer to
[IAsyncOperation](/uwp/api/windows.foundation.iasyncoperation-1)&lt;[WebTokenRequestResult](/uwp/api/windows.security.authentication.web.core.webtokenrequestresult)&gt;.
On successful return from this method, the pointer will be set to the
asynchronous request operation object for the request operation just started.

## -returns

A status code for the attempt to start the asynchronous request operation.

## -remarks

This method is the equivalent for desktop apps of
[WebAuthenticationCoreManager.RequestTokenAsync(WebTokenRequest)](/uwp/api/windows.security.authentication.web.core.webauthenticationcoremanager.requesttokenasync#Windows_Security_Authentication_Web_Core_WebAuthenticationCoreManager_RequestTokenAsync_Windows_Security_Authentication_Web_Core_WebTokenRequest_).

## -see-also
[Web account management code sample](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/WebAccountManagement), [RequestTokenWithWebAccountForWindowAsync](nf-webauthenticationcoremanagerinterop-iwebauthenticationcoremanagerinterop-requesttokenwithwebaccountforwindowasync)
