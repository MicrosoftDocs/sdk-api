---
UID: NF:webapplication.IWebApplicationNavigationEvents.NavigateError
title: IWebApplicationNavigationEvents::NavigateError (webapplication.h)
description: Fired when a binding error occurs (window or frameset element).
helpviewer_keywords: ["IWebApplicationNavigationEvents interface [Debugging Windows Store apps]","NavigateError method","IWebApplicationNavigationEvents.NavigateError","IWebApplicationNavigationEvents::NavigateError","NavigateError","NavigateError method [Debugging Windows Store apps]","NavigateError method [Debugging Windows Store apps]","IWebApplicationNavigationEvents interface","debug.iwebapplicationnavigationevents_navigateerror","webapplication/IWebApplicationNavigationEvents::NavigateError"]
old-location: debug\iwebapplicationnavigationevents_navigateerror.htm
tech.root: debug
ms.assetid: 1c6e34e8-e14f-4b6c-ad83-140a7141cf64
ms.date: 12/05/2018
ms.keywords: IWebApplicationNavigationEvents interface [Debugging Windows Store apps],NavigateError method, IWebApplicationNavigationEvents.NavigateError, IWebApplicationNavigationEvents::NavigateError, NavigateError, NavigateError method [Debugging Windows Store apps], NavigateError method [Debugging Windows Store apps],IWebApplicationNavigationEvents interface, debug.iwebapplicationnavigationevents_navigateerror, webapplication/IWebApplicationNavigationEvents::NavigateError
req.header: webapplication.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Webapplication.idl
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
 - IWebApplicationNavigationEvents::NavigateError
 - webapplication/IWebApplicationNavigationEvents::NavigateError
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - webapplication.h
api_name:
 - IWebApplicationNavigationEvents.NavigateError
---

# IWebApplicationNavigationEvents::NavigateError


## -description

Fired when a binding error occurs (window or frameset element).

## -parameters

### -param htmlWindow [in]

Type: <b><a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa741505(v=vs.85)">IHTMLWindow2</a>*</b>

The window ro frame in which the navigation error occurred.

### -param url [in]

Type: <b>LPCWSTR</b>

The URL for which navigation failed.

### -param targetFrameName [in]

Type: <b>LPCWSTR</b>

The name of the frame in which the navigation error occurred. The value is <b>null</b> if no named frame was targeted.

### -param statusCode [in]

Type: <b>DWORD</b>

The error code. Could be a <b>HRESULT</b> or a HTTP status code.

## -returns

Type: <b>HRESULT</b>

Ignored by the host. If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/webapplication/nn-webapplication-iwebapplicationnavigationevents">IWebApplicationNavigationEvents</a>