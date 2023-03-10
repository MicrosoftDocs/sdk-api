---
UID: NF:webauthenticationcoremanagerinterop.IWebAuthenticationCoreManagerInterop.RequestTokenForWindowAsync
title: IWebAuthenticationCoreManagerInterop::RequestTokenForWindowAsync
description: Asynchronously requests a token from a web account provider. If necessary, the user is prompted to enter their credentials. (IWebAuthenticationCoreManagerInterop::RequestTokenForWindowAsync)
helpviewer_keywords: ["IWebAuthenticationCoreManagerInterop::RequestTokenForWindowAsync"]
ms.date: 5/28/2019
ms.keywords: IWebAuthenticationCoreManagerInterop::RequestTokenForWindowAsync
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
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
tech.root: winrt
f1_keywords:
 - IWebAuthenticationCoreManagerInterop::RequestTokenForWindowAsync
 - webauthenticationcoremanagerinterop/IWebAuthenticationCoreManagerInterop::RequestTokenForWindowAsync
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - webauthenticationcoremanagerinterop.h
api_name:
 - IWebAuthenticationCoreManagerInterop::RequestTokenForWindowAsync
---

## -description

Asynchronously requests a token from a web account provider. If necessary, the user is prompted to enter their credentials.

## -parameters

### -param appWindow

Type: **[HWND](/windows/win32/winprog/windows-data-types)**

The window to be used as the owner for the window prompting the user for credentials, in case such a window becomes necessary.

### -param request

Type: **[IInspectable](../inspectable/nn-inspectable-iinspectable.md)\***

The web token request, given as an instance of the
[WebTokenRequest](/uwp/api/windows.security.authentication.web.core.webtokenrequest)
class type-casted to the [IInspectable](../inspectable/nn-inspectable-iinspectable.md)
interface.

### -param riid

Type: **REFIID**

Must be a reference to the [interface identifier (IID)](/openspecs/windows_protocols/ms-oaut/5583e1b8-454c-4147-9f56-f72416a15bee#gt_76ad3105-3f05-479d-a40c-c9c8fa2ebd83) for the interface
[IAsyncOperation](/uwp/api/windows.foundation.iasyncoperation-1)\<[WebTokenRequestResult](/uwp/api/windows.security.authentication.web.core.webtokenrequestresult)\>.
This IID is automatically generated, and you can obtain it using code like this:

```cppwinrt
using winrt::Windows::Foundation::IAsyncOperation;
using winrt::Windows::Security::Authentication::Web::Core::WebTokenRequestResult;

constexpr winrt::guid iidAsyncRequestResult{ winrt::guid_of<IAsyncOperation<WebTokenRequestResult>>() };
```

### -param asyncInfo

Type: **void\*\***

The address of a pointer to [IAsyncOperation](/uwp/api/windows.foundation.iasyncoperation-1)\<[WebTokenRequestResult](/uwp/api/windows.security.authentication.web.core.webtokenrequestresult)\>. On successful return from this method, the pointer will be set to the asynchronous request operation object for the request operation just started.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

A status code for the attempt to start the asynchronous request operation.

## -remarks

This method is the equivalent for desktop apps of
[WebAuthenticationCoreManager.RequestTokenAsync(WebTokenRequest)](/uwp/api/windows.security.authentication.web.core.webauthenticationcoremanager.requesttokenasync#Windows_Security_Authentication_Web_Core_WebAuthenticationCoreManager_RequestTokenAsync_Windows_Security_Authentication_Web_Core_WebTokenRequest_).

## -see-also

- [Web account management sample app](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/WebAccountManagement)
- [RequestTokenWithWebAccountForWindowAsync](nf-webauthenticationcoremanagerinterop-iwebauthenticationcoremanagerinterop-requesttokenwithwebaccountforwindowasync.md)
