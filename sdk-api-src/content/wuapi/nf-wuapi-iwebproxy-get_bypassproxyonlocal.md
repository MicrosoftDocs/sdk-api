---
UID: NF:wuapi.IWebProxy.get_BypassProxyOnLocal
title: IWebProxy::get_BypassProxyOnLocal
author: windows-sdk-content
description: Gets and sets a Boolean value that indicates whether local addresses bypass the proxy server.
old-location: wua\iwebproxy_bypassproxyonlocal.htm
old-project: Wua_Sdk
ms.assetid: 541626ca-0b68-41cd-8f20-5ffd034fc878
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: BypassProxyOnLocal property [Windows Update Agent], BypassProxyOnLocal property [Windows Update Agent],IWebProxy interface, IWebProxy interface [Windows Update Agent],BypassProxyOnLocal property, IWebProxy.BypassProxyOnLocal, IWebProxy.get_BypassProxyOnLocal, IWebProxy::BypassProxyOnLocal, IWebProxy::get_BypassProxyOnLocal, IWebProxy::put_BypassProxyOnLocal, get_BypassProxyOnLocal, wua.iwebproxy_bypassproxyonlocal, wuapi/IWebProxy::BypassProxyOnLocal, wuapi/IWebProxy::get_BypassProxyOnLocal, wuapi/IWebProxy::put_BypassProxyOnLocal
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: UpdateType
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
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IWebProxy::get_BypassProxyOnLocal


## -description


Gets and sets a Boolean value that indicates whether local addresses  bypass the proxy server.

This property is read/write.


## -parameters


## -remarks



The value of the <b>BypassProxyOnLocal</b> property is ignored if the value of the <a href="https://msdn.microsoft.com/cd222133-e44b-453a-9fbf-72f609cb2d4b">AutoDetect</a> property is set to <b>VARIANT_TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/acc09635-7370-475f-9c3a-a5faaa8d576a">IWebProxy</a>
 

 

