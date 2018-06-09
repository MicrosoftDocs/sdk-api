---
UID: NF:wuapi.IWebProxy.put_AutoDetect
title: IWebProxy::put_AutoDetect
author: windows-sdk-content
description: Gets and sets a Boolean value that indicates whether IWebProxy automatically detects proxy settings.
old-location: wua\iwebproxy_autodetect.htm
old-project: Wua_Sdk
ms.assetid: cd222133-e44b-453a-9fbf-72f609cb2d4b
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: AutoDetect property [Windows Update Agent], AutoDetect property [Windows Update Agent],IWebProxy interface, IWebProxy interface [Windows Update Agent],AutoDetect property, IWebProxy.AutoDetect, IWebProxy.put_AutoDetect, IWebProxy::AutoDetect, IWebProxy::get_AutoDetect, IWebProxy::put_AutoDetect, put_AutoDetect, wua.iwebproxy_autodetect, wuapi/IWebProxy::AutoDetect, wuapi/IWebProxy::get_AutoDetect, wuapi/IWebProxy::put_AutoDetect
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
 - IWebProxy.AutoDetect
 - IWebProxy.get_AutoDetect
 - IWebProxy.put_AutoDetect
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IWebProxy::put_AutoDetect


## -description


Gets and sets a Boolean value that indicates whether <a href="https://msdn.microsoft.com/acc09635-7370-475f-9c3a-a5faaa8d576a">IWebProxy</a>  automatically detects proxy settings.

This property is read/write.


## -parameters


## -remarks



The values of the <a href="https://msdn.microsoft.com/library/windows/hardware/mt427295">Address</a>, <a href="https://msdn.microsoft.com/a93742d2-73ce-4e7b-a000-592fd588cb1f">BypassList</a>, and <a href="https://msdn.microsoft.com/541626ca-0b68-41cd-8f20-5ffd034fc878">BypassProxyOnLocal</a> properties are ignored if the value of the <b>AutoDetect</b> property is set to <b>VARIANT_TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/acc09635-7370-475f-9c3a-a5faaa8d576a">IWebProxy</a>
 

 

