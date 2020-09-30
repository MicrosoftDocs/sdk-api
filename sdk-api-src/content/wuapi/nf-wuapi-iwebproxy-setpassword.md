---
UID: NF:wuapi.IWebProxy.SetPassword
title: IWebProxy::SetPassword (wuapi.h)
description: Sets the password to submit to the proxy server for authentication.
helpviewer_keywords: ["IWebProxy interface [Windows Update Agent]","SetPassword method","IWebProxy.SetPassword","IWebProxy::SetPassword","SetPassword","SetPassword method [Windows Update Agent]","SetPassword method [Windows Update Agent]","IWebProxy interface","wua.iwebproxy_setpassword","wuapi/IWebProxy::SetPassword"]
old-location: wua\iwebproxy_setpassword.htm
tech.root: wua
ms.assetid: 59b500f1-2015-4f72-9be5-c2f57462dff0
ms.date: 12/05/2018
ms.keywords: IWebProxy interface [Windows Update Agent],SetPassword method, IWebProxy.SetPassword, IWebProxy::SetPassword, SetPassword, SetPassword method [Windows Update Agent], SetPassword method [Windows Update Agent],IWebProxy interface, wua.iwebproxy_setpassword, wuapi/IWebProxy::SetPassword
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWebProxy::SetPassword
 - wuapi/IWebProxy::SetPassword
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IWebProxy.SetPassword
---

# IWebProxy::SetPassword


## -description

Sets the password to submit to the proxy server for authentication.

## -parameters

### -param value

The password to submit to the proxy server for authentication.

## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iwebproxy">IWebProxy</a>