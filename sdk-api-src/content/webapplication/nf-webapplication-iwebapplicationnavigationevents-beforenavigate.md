---
UID: NF:webapplication.IWebApplicationNavigationEvents.BeforeNavigate
title: IWebApplicationNavigationEvents::BeforeNavigate (webapplication.h)
description: Fired before navigate occurs in the given host (window or frameset element).
helpviewer_keywords: ["BeforeNavigate","BeforeNavigate method [Debugging Windows Store apps]","BeforeNavigate method [Debugging Windows Store apps]","IWebApplicationNavigationEvents interface","IWebApplicationNavigationEvents interface [Debugging Windows Store apps]","BeforeNavigate method","IWebApplicationNavigationEvents.BeforeNavigate","IWebApplicationNavigationEvents::BeforeNavigate","debug.iwebapplicationnavigationevents_beforenavigate","webapplication/IWebApplicationNavigationEvents::BeforeNavigate"]
old-location: debug\iwebapplicationnavigationevents_beforenavigate.htm
tech.root: debug
ms.assetid: 1088bfa3-0a20-4156-90ff-50129e903052
ms.date: 12/05/2018
ms.keywords: BeforeNavigate, BeforeNavigate method [Debugging Windows Store apps], BeforeNavigate method [Debugging Windows Store apps],IWebApplicationNavigationEvents interface, IWebApplicationNavigationEvents interface [Debugging Windows Store apps],BeforeNavigate method, IWebApplicationNavigationEvents.BeforeNavigate, IWebApplicationNavigationEvents::BeforeNavigate, debug.iwebapplicationnavigationevents_beforenavigate, webapplication/IWebApplicationNavigationEvents::BeforeNavigate
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
 - IWebApplicationNavigationEvents::BeforeNavigate
 - webapplication/IWebApplicationNavigationEvents::BeforeNavigate
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
 - IWebApplicationNavigationEvents.BeforeNavigate
---

# IWebApplicationNavigationEvents::BeforeNavigate


## -description

Fired before navigate occurs in the given host (window or frameset element).

## -parameters

### -param htmlWindow [in]

Type: <b><a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa741505(v=vs.85)">IHTMLWindow2</a>*</b>

The window or frame in which the navigation is about occur.

### -param url [in]

Type: <b>LPCWSTR</b>

The URL to navigate to.

### -param navigationFlags [in]

Type: <b>DWORD</b>

Flags related to the current navigation.

### -param targetFrameName [in]

Type: <b>LPCWSTR</b>

The name of the frame in which the navigation is about to occur. The value is <b>null</b> if no named frame is targeted.

## -returns

Type: <b>HRESULT</b>

Ignored by the host. If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/webapplication/nn-webapplication-iwebapplicationnavigationevents">IWebApplicationNavigationEvents</a>