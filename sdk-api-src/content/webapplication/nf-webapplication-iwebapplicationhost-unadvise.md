---
UID: NF:webapplication.IWebApplicationHost.Unadvise
title: IWebApplicationHost::Unadvise (webapplication.h)
description: Removes a previously established connection.
helpviewer_keywords: ["IWebApplicationHost interface [Debugging Windows Store apps]","Unadvise method","IWebApplicationHost.Unadvise","IWebApplicationHost::Unadvise","Unadvise","Unadvise method [Debugging Windows Store apps]","Unadvise method [Debugging Windows Store apps]","IWebApplicationHost interface","debug.iwebapplicationhost_unadvise","webapplication/IWebApplicationHost::Unadvise"]
old-location: debug\iwebapplicationhost_unadvise.htm
tech.root: debug
ms.assetid: daab1a3f-1f84-4559-bdc0-be8f1fb28904
ms.date: 12/05/2018
ms.keywords: IWebApplicationHost interface [Debugging Windows Store apps],Unadvise method, IWebApplicationHost.Unadvise, IWebApplicationHost::Unadvise, Unadvise, Unadvise method [Debugging Windows Store apps], Unadvise method [Debugging Windows Store apps],IWebApplicationHost interface, debug.iwebapplicationhost_unadvise, webapplication/IWebApplicationHost::Unadvise
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
 - IWebApplicationHost::Unadvise
 - webapplication/IWebApplicationHost::Unadvise
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
 - IWebApplicationHost.Unadvise
---

# IWebApplicationHost::Unadvise


## -description

Removes a previously established connection.

## -parameters

### -param cookie [in]

Type: <b>DWORD</b>

A connection token previously returned from the <a href="/previous-versions/windows/desktop/debug_wwahost/iwebapplicationhost-advise">Advise</a> method.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/webapplication/nn-webapplication-iwebapplicationhost">IWebApplicationHost</a>



<a href="/previous-versions/windows/desktop/debug_wwahost/iwebapplicationhost-advise">IWebApplicationHost::Advise</a>