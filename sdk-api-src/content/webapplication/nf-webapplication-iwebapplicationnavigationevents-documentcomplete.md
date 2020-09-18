---
UID: NF:webapplication.IWebApplicationNavigationEvents.DocumentComplete
title: IWebApplicationNavigationEvents::DocumentComplete (webapplication.h)
description: Fired when the document being navigated to reaches ReadyState_Complete.
helpviewer_keywords: ["DocumentComplete","DocumentComplete method [Debugging Windows Store apps]","DocumentComplete method [Debugging Windows Store apps]","IWebApplicationNavigationEvents interface","IWebApplicationNavigationEvents interface [Debugging Windows Store apps]","DocumentComplete method","IWebApplicationNavigationEvents.DocumentComplete","IWebApplicationNavigationEvents::DocumentComplete","debug.iwebapplicationnavigationevents_documentcomplete","webapplication/IWebApplicationNavigationEvents::DocumentComplete"]
old-location: debug\iwebapplicationnavigationevents_documentcomplete.htm
tech.root: debug
ms.assetid: 18dabd8a-d35c-4095-985d-bf712c539df8
ms.date: 12/05/2018
ms.keywords: DocumentComplete, DocumentComplete method [Debugging Windows Store apps], DocumentComplete method [Debugging Windows Store apps],IWebApplicationNavigationEvents interface, IWebApplicationNavigationEvents interface [Debugging Windows Store apps],DocumentComplete method, IWebApplicationNavigationEvents.DocumentComplete, IWebApplicationNavigationEvents::DocumentComplete, debug.iwebapplicationnavigationevents_documentcomplete, webapplication/IWebApplicationNavigationEvents::DocumentComplete
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
 - IWebApplicationNavigationEvents::DocumentComplete
 - webapplication/IWebApplicationNavigationEvents::DocumentComplete
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
 - IWebApplicationNavigationEvents.DocumentComplete
---

# IWebApplicationNavigationEvents::DocumentComplete


## -description

Fired when the document being navigated to reaches ReadyState_Complete.

## -parameters

### -param htmlWindow [in]

Type: <b><a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa741505(v=vs.85)">IHTMLWindow2</a>*</b>

The window or frame in which the document is loaded.

### -param url [in]

Type: <b>LPCWSTR</b>

The URL of the document.

## -returns

Type: <b>HRESULT</b>

Ignored by the host. If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/webapplication/nn-webapplication-iwebapplicationnavigationevents">IWebApplicationNavigationEvents</a>