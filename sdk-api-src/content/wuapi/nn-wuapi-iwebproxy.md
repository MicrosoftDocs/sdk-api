---
UID: NN:wuapi.IWebProxy
title: IWebProxy (wuapi.h)
description: Contains the HTTP proxy settings.
helpviewer_keywords: ["IWebProxy","IWebProxy interface [Windows Update Agent]","IWebProxy interface [Windows Update Agent]","described","wua.iwebproxy","wuapi/IWebProxy"]
old-location: wua\iwebproxy.htm
tech.root: wua
ms.assetid: acc09635-7370-475f-9c3a-a5faaa8d576a
ms.date: 12/05/2018
ms.keywords: IWebProxy, IWebProxy interface [Windows Update Agent], IWebProxy interface [Windows Update Agent],described, wua.iwebproxy, wuapi/IWebProxy
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
 - IWebProxy
 - wuapi/IWebProxy
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
 - IWebProxy
---

# IWebProxy interface


## -description

Contains the HTTP proxy settings.
<div class="alert"><b>Important</b>  This interface is not supported on Windows 10 and Windows Server 2016. See the remarks for more details.</div><div> </div>

## -inheritance

The <b>IWebProxy</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWebProxy</b> also has these types of members:

## -remarks

You can create an instance of this interface by using the WebProxy coclass. Use the Microsoft.Update.WebProxy program identifier to create the object.

<div class="alert"><b>Important</b>  This interface is not supported on Windows 10 and Windows Server 2016. To configure proxy settings on  these operating systems (including proxy settings for  Windows Update Agent), use the  <b>Proxy</b> page of the <b>Network &amp; Internet</b> section in <b>Settings</b>. You can optionally use a <a href="https://en.wikipedia.org/wiki/Proxy_auto-config">proxy auto-config script</a> to apply settings. If you configure proxy settings, be sure to allow access to the domains used by Windows Update listed in <a href="https://support.microsoft.com/help/3084568/">this article</a>.</div>
<div> </div>
