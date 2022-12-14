---
UID: NF:wuapi.IWebProxy.put_BypassList
title: IWebProxy::put_BypassList (wuapi.h)
description: Gets and sets a collection of addresses that do not use the proxy server. (Put)
helpviewer_keywords: ["BypassList property [Windows Update Agent]","BypassList property [Windows Update Agent]","IWebProxy interface","IWebProxy interface [Windows Update Agent]","BypassList property","IWebProxy.BypassList","IWebProxy.put_BypassList","IWebProxy::BypassList","IWebProxy::get_BypassList","IWebProxy::put_BypassList","put_BypassList","wua.iwebproxy_bypasslist","wuapi/IWebProxy::BypassList","wuapi/IWebProxy::get_BypassList","wuapi/IWebProxy::put_BypassList"]
old-location: wua\iwebproxy_bypasslist.htm
tech.root: wua
ms.assetid: a93742d2-73ce-4e7b-a000-592fd588cb1f
ms.date: 12/05/2018
ms.keywords: BypassList property [Windows Update Agent], BypassList property [Windows Update Agent],IWebProxy interface, IWebProxy interface [Windows Update Agent],BypassList property, IWebProxy.BypassList, IWebProxy.put_BypassList, IWebProxy::BypassList, IWebProxy::get_BypassList, IWebProxy::put_BypassList, put_BypassList, wua.iwebproxy_bypasslist, wuapi/IWebProxy::BypassList, wuapi/IWebProxy::get_BypassList, wuapi/IWebProxy::put_BypassList
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
 - IWebProxy::put_BypassList
 - wuapi/IWebProxy::put_BypassList
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
 - IWebProxy.BypassList
 - IWebProxy.get_BypassList
 - IWebProxy.put_BypassList
---

# IWebProxy::put_BypassList


## -description

Gets and sets a collection of addresses that do not use the proxy server.

This property is read/write.

## -parameters

## -remarks

The value of the <b>BypassList</b> property is ignored if the value of the <a href="/windows/desktop/api/wuapi/nf-wuapi-iwebproxy-get_autodetect">AutoDetect</a> property is set to <b>VARIANT_TRUE</b>.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iwebproxy">IWebProxy</a>
