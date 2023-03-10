---
UID: NF:wuapi.IWebProxy.get_BypassProxyOnLocal
title: IWebProxy::get_BypassProxyOnLocal (wuapi.h)
description: Gets and sets a Boolean value that indicates whether local addresses bypass the proxy server. (Get)
helpviewer_keywords: ["BypassProxyOnLocal property [Windows Update Agent]","BypassProxyOnLocal property [Windows Update Agent]","IWebProxy interface","IWebProxy interface [Windows Update Agent]","BypassProxyOnLocal property","IWebProxy.BypassProxyOnLocal","IWebProxy.get_BypassProxyOnLocal","IWebProxy::BypassProxyOnLocal","IWebProxy::get_BypassProxyOnLocal","IWebProxy::put_BypassProxyOnLocal","get_BypassProxyOnLocal","wua.iwebproxy_bypassproxyonlocal","wuapi/IWebProxy::BypassProxyOnLocal","wuapi/IWebProxy::get_BypassProxyOnLocal","wuapi/IWebProxy::put_BypassProxyOnLocal"]
old-location: wua\iwebproxy_bypassproxyonlocal.htm
tech.root: wua
ms.assetid: 541626ca-0b68-41cd-8f20-5ffd034fc878
ms.date: 12/05/2018
ms.keywords: BypassProxyOnLocal property [Windows Update Agent], BypassProxyOnLocal property [Windows Update Agent],IWebProxy interface, IWebProxy interface [Windows Update Agent],BypassProxyOnLocal property, IWebProxy.BypassProxyOnLocal, IWebProxy.get_BypassProxyOnLocal, IWebProxy::BypassProxyOnLocal, IWebProxy::get_BypassProxyOnLocal, IWebProxy::put_BypassProxyOnLocal, get_BypassProxyOnLocal, wua.iwebproxy_bypassproxyonlocal, wuapi/IWebProxy::BypassProxyOnLocal, wuapi/IWebProxy::get_BypassProxyOnLocal, wuapi/IWebProxy::put_BypassProxyOnLocal
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
 - IWebProxy::get_BypassProxyOnLocal
 - wuapi/IWebProxy::get_BypassProxyOnLocal
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
 - IWebProxy.BypassProxyOnLocal
 - IWebProxy.get_BypassProxyOnLocal
 - IWebProxy.put_BypassProxyOnLocal
---

# IWebProxy::get_BypassProxyOnLocal


## -description

Gets and sets a Boolean value that indicates whether local addresses  bypass the proxy server.

This property is read/write.

## -parameters

## -remarks

The value of the <b>BypassProxyOnLocal</b> property is ignored if the value of the <a href="/windows/desktop/api/wuapi/nf-wuapi-iwebproxy-get_autodetect">AutoDetect</a> property is set to <b>VARIANT_TRUE</b>.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iwebproxy">IWebProxy</a>
