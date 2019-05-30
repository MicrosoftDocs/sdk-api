---
UID: NF:webauthenticationcoremanagerinterop.IWebAuthenticationCoreManagerInterop.RequestTokenWithWebAccountForWindowAsync
title: IWebAuthenticationCoreManagerInterop::RequestTokenWithWebAccountForWindowAsync
description: Asynchronously requests a token from a web account provider. If necessary, the user is prompted to enter their credentials.
ms.date: 5/28/2019
ms.keywords: IWebAuthenticationCoreManagerInterop::RequestTokenWithWebAccountForWindowAsync
ms.topic: language-reference
targetos: Windows
product: Windows
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
 - IWebAuthenticationCoreManagerInterop::RequestTokenWithWebAccountForWindowAsync
tech.root: winrt
---

## -description

Asynchronously requests a token from a web account provider. If necessary, the user is prompted to enter their credentials.

## -parameters

### -param appWindow

Type: [HWND](https://docs.microsoft.com/windows/desktop/winprog/windows-data-types)

The app window.

### -param request

Type: [IInspectable](../inspectable/nn-inspectable-iinspectable.md)\*

The web token request.

### -param webAccount

Type: [IInspectable](../inspectable/nn-inspectable-iinspectable.md)\*

The web account for the request.

### -param riid

Type: [REFIID](https://docs.microsoft.com/openspecs/windows_protocols/ms-oaut/bbde795f-5398-42d8-9f59-3613da03c318)

The interface identifier.

### -param asyncInfo

Type: **void**\*\*

The asynchronous operation.

## -returns

Type: [HRESULT](https://docs.microsoft.com/windows/desktop/winprog/windows-data-types)

The result of the operation.

## -remarks

## -see-also
