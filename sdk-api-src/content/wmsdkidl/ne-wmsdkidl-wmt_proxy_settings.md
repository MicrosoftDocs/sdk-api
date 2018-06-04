---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WMT_PROXY_SETTINGS enumeration


## -description



The <b>WMT_PROXY_SETTINGS</b> enumeration type defines network proxy settings for use with a reader object.




## -enum-fields




### -field WMT_PROXY_SETTING_NONE

No proxy settings will be used.


### -field WMT_PROXY_SETTING_MANUAL

Proxy settings will be explicitly set.


### -field WMT_PROXY_SETTING_AUTO

Proxy settings will be automatically negotiated.


### -field WMT_PROXY_SETTING_BROWSER

The browser will negotiate the proxy settings. This applies only when using HTTP.


### -field WMT_PROXY_SETTING_MAX


## -remarks



The WMT_PROXY_SETTING_BROWSER setting applies only to the HTTP protocol.

This enumeration is used directly in <b>GetProxySettings</b> and <b>SetProxySettings</b>, and referenced in several other methods of the <b>IWMReaderNetworkConfig</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff545452">Enumeration Types</a>



<a href="https://msdn.microsoft.com/5fdfc651-05f5-48b3-aeaf-4557c72bc0c0">IWMReaderNetworkConfig::GetProxySettings</a>



<a href="https://msdn.microsoft.com/fe5bc4f2-860a-42e8-b9f1-cd3d8af619c2">IWMReaderNetworkConfig::SetProxySettings</a>
 

 

