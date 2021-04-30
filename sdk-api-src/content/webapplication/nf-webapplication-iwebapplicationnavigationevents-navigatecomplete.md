---
UID: NF:webapplication.IWebApplicationNavigationEvents.NavigateComplete
title: IWebApplicationNavigationEvents::NavigateComplete (webapplication.h)
description: Fired when the document being navigated to becomes visible and enters the navigation stack.
helpviewer_keywords: ["IWebApplicationNavigationEvents interface [Debugging Windows Store apps]","NavigateComplete method","IWebApplicationNavigationEvents.NavigateComplete","IWebApplicationNavigationEvents::NavigateComplete","NavigateComplete","NavigateComplete method [Debugging Windows Store apps]","NavigateComplete method [Debugging Windows Store apps]","IWebApplicationNavigationEvents interface","debug.iwebapplicationnavigationevents_navigatecomplete","webapplication/IWebApplicationNavigationEvents::NavigateComplete"]
old-location: debug\iwebapplicationnavigationevents_navigatecomplete.htm
tech.root: debug
ms.assetid: 51a80227-69ec-4f12-8d19-d2b932fbbfc0
ms.date: 12/05/2018
ms.keywords: IWebApplicationNavigationEvents interface [Debugging Windows Store apps],NavigateComplete method, IWebApplicationNavigationEvents.NavigateComplete, IWebApplicationNavigationEvents::NavigateComplete, NavigateComplete, NavigateComplete method [Debugging Windows Store apps], NavigateComplete method [Debugging Windows Store apps],IWebApplicationNavigationEvents interface, debug.iwebapplicationnavigationevents_navigatecomplete, webapplication/IWebApplicationNavigationEvents::NavigateComplete
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
 - IWebApplicationNavigationEvents::NavigateComplete
 - webapplication/IWebApplicationNavigationEvents::NavigateComplete
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
 - IWebApplicationNavigationEvents.NavigateComplete
---

# IWebApplicationNavigationEvents::NavigateComplete


## -description

Fired when the document being navigated to becomes visible and enters the navigation stack.

## -parameters

### -param htmlWindow [in]

Type: <b><a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa741505(v=vs.85)">IHTMLWindow2</a>*</b>

The window or frame in which the navigation is occurred.

### -param url [in]

Type: <b>LPCWSTR</b>

The URL which was navigated to

## -returns

Type: <b>HRESULT</b>

Ignored by the host. If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/webapplication/nn-webapplication-iwebapplicationnavigationevents">IWebApplicationNavigationEvents</a>