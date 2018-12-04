---
UID: NF:wuapi.IWebProxy.put_Address
title: IWebProxy::put_Address
author: windows-sdk-content
description: Gets and sets the address and the decimal port number of the proxy server.
old-location: wua\iwebproxy_address.htm
tech.root: wua_sdk
ms.assetid: ed8c899f-5080-435a-8577-7e92a54738ad
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: Address property [Windows Update Agent], Address property [Windows Update Agent],IWebProxy interface, IWebProxy interface [Windows Update Agent],Address property, IWebProxy.Address, IWebProxy.put_Address, IWebProxy::Address, IWebProxy::get_Address, IWebProxy::put_Address, put_Address, wua.iwebproxy_address, wuapi/IWebProxy::Address, wuapi/IWebProxy::get_Address, wuapi/IWebProxy::put_Address
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWebProxy.Address
 - IWebProxy.get_Address
 - IWebProxy.put_Address
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWebProxy::put_Address


## -description


Gets and sets the address and the decimal port number of the proxy server.

This property is read/write.


## -parameters


## -remarks



The value of the <b>Address</b> property is ignored if the value of the <a href="https://msdn.microsoft.com/cd222133-e44b-453a-9fbf-72f609cb2d4b">AutoDetect</a> property is set to <b>VARIANT_TRUE</b>.
When <b>Address</b> is a null reference (for example, if you specified Nothing in Visual Basic), all the requests bypass the proxy. The requests connect directly to the destination host.




## -see-also




<a href="https://msdn.microsoft.com/acc09635-7370-475f-9c3a-a5faaa8d576a">IWebProxy</a>
 

 

