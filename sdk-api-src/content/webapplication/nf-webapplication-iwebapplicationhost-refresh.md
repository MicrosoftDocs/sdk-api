---
UID: NF:webapplication.IWebApplicationHost.Refresh
title: IWebApplicationHost::Refresh (webapplication.h)
description: Refreshes the current document without sending a 'Pragma:no-cache' HTTP header to the server.
helpviewer_keywords: ["IWebApplicationHost interface [Debugging Windows Store apps]","Refresh method","IWebApplicationHost.Refresh","IWebApplicationHost::Refresh","Refresh","Refresh method [Debugging Windows Store apps]","Refresh method [Debugging Windows Store apps]","IWebApplicationHost interface","debug.iwebapplicationhost_refresh","webapplication/IWebApplicationHost::Refresh"]
old-location: debug\iwebapplicationhost_refresh.htm
tech.root: debug
ms.assetid: 66f94cc9-9407-4844-a100-8144fc6f45ce
ms.date: 12/05/2018
ms.keywords: IWebApplicationHost interface [Debugging Windows Store apps],Refresh method, IWebApplicationHost.Refresh, IWebApplicationHost::Refresh, Refresh, Refresh method [Debugging Windows Store apps], Refresh method [Debugging Windows Store apps],IWebApplicationHost interface, debug.iwebapplicationhost_refresh, webapplication/IWebApplicationHost::Refresh
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
 - IWebApplicationHost::Refresh
 - webapplication/IWebApplicationHost::Refresh
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
 - IWebApplicationHost.Refresh
---

# IWebApplicationHost::Refresh


## -description

Refreshes the current document without sending a 'Pragma:no-cache' HTTP header to the server.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Use this method when the currently executing code is outside of the activation path. If the code is executing inside the activation path, use <a href="/previous-versions/windows/desktop/api/webapplication/nf-webapplication-iwebapplicationactivation-cancelpendingactivation">IWebApplicationActivation::CancelPendingActivation</a> instead.

## -see-also

<a href="/previous-versions/windows/desktop/api/webapplication/nn-webapplication-iwebapplicationhost">IWebApplicationHost</a>
