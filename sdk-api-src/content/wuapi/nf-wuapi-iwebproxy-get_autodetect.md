---
UID: NF:wuapi.IWebProxy.get_AutoDetect
title: IWebProxy::get_AutoDetect (wuapi.h)
description: Gets and sets a Boolean value that indicates whether IWebProxy automatically detects proxy settings.
old-location: wua\iwebproxy_autodetect.htm
tech.root: Wua_Sdk
ms.assetid: cd222133-e44b-453a-9fbf-72f609cb2d4b
ms.date: 12/05/2018
ms.keywords: AutoDetect property [Windows Update Agent], AutoDetect property [Windows Update Agent],IWebProxy interface, IWebProxy interface [Windows Update Agent],AutoDetect property, IWebProxy.AutoDetect, IWebProxy.get_AutoDetect, IWebProxy::AutoDetect, IWebProxy::get_AutoDetect, IWebProxy::put_AutoDetect, get_AutoDetect, wua.iwebproxy_autodetect, wuapi/IWebProxy::AutoDetect, wuapi/IWebProxy::get_AutoDetect, wuapi/IWebProxy::put_AutoDetect
f1_keywords:
- wuapi/IWebProxy.AutoDetect
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wuapi.dll
api_name:
- IWebProxy.AutoDetect
- IWebProxy.get_AutoDetect
- IWebProxy.put_AutoDetect
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWebProxy::get_AutoDetect


## -description


Gets and sets a Boolean value that indicates whether <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iwebproxy">IWebProxy</a>  automatically detects proxy settings.

This property is read/write.


## -parameters


## -remarks



The values of the <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iwebproxy-get_address">Address</a>, <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iwebproxy-get_bypasslist">BypassList</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-iwebproxy-get_bypassproxyonlocal">BypassProxyOnLocal</a> properties are ignored if the value of the <b>AutoDetect</b> property is set to <b>VARIANT_TRUE</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nn-wuapi-iwebproxy">IWebProxy</a>
 

 

