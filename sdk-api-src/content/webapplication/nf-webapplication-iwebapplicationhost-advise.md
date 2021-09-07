---
UID: NF:webapplication.IWebApplicationHost.Advise
title: IWebApplicationHost::Advise (webapplication.h)
description: Establishes a connection to allow a client to receive events.
helpviewer_keywords: ["Advise","Advise method [Debugging Windows Store apps]","Advise method [Debugging Windows Store apps]","IWebApplicationHost interface","IWebApplicationHost interface [Debugging Windows Store apps]","Advise method","IWebApplicationHost.Advise","IWebApplicationHost::Advise","debug.iwebapplicationhost_advise","webapplication/IWebApplicationHost::Advise"]
old-location: debug\iwebapplicationhost_advise.htm
tech.root: debug
ms.assetid: 94c016cb-f043-4ea6-a5d1-f3486b55c97f
ms.date: 12/05/2018
ms.keywords: Advise, Advise method [Debugging Windows Store apps], Advise method [Debugging Windows Store apps],IWebApplicationHost interface, IWebApplicationHost interface [Debugging Windows Store apps],Advise method, IWebApplicationHost.Advise, IWebApplicationHost::Advise, debug.iwebapplicationhost_advise, webapplication/IWebApplicationHost::Advise
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
 - IWebApplicationHost::Advise
 - webapplication/IWebApplicationHost::Advise
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
 - IWebApplicationHost.Advise
---

# IWebApplicationHost::Advise


## -description

Establishes a connection to allow a client to receive events.

## -parameters

### -param interfaceId [in]

Type: <b>REFIID</b>

The identifier of the event interface.

### -param callback [in]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>*</b>

The caller's event interface.

### -param cookie [out]

Type: <b>DWORD*</b>

A token that uniquely identifies this connection.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/webapplication/nn-webapplication-iwebapplicationhost">IWebApplicationHost</a>



<a href="/previous-versions/windows/desktop/debug_wwahost/iwebapplicationhost-unadvise">IWebApplicationHost::Unadvise</a>