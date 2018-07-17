---
UID: NE:wmsdkidl.WMT_PROXY_SETTINGS
title: WMT_PROXY_SETTINGS
author: windows-sdk-content
description: The WMT_PROXY_SETTINGS enumeration type defines network proxy settings for use with a reader object.
old-location: wmformat\wmt_proxy_settings.htm
old-project: wmformat
ms.assetid: a055259e-e207-426c-b6ca-a27bc3d0e88c
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: WMT_PROXY_SETTINGS, WMT_PROXY_SETTINGS enumeration [windows Media Format], WMT_PROXY_SETTING_AUTO, WMT_PROXY_SETTING_BROWSER, WMT_PROXY_SETTING_MANUAL, WMT_PROXY_SETTING_MAX, WMT_PROXY_SETTING_NONE, enumeration [windows Media Format], wmformat.wmt_proxy_settings, wmsdkidl/WMT_PROXY_SETTINGS, wmsdkidl/WMT_PROXY_SETTING_AUTO, wmsdkidl/WMT_PROXY_SETTING_BROWSER, wmsdkidl/WMT_PROXY_SETTING_MANUAL, wmsdkidl/WMT_PROXY_SETTING_MAX, wmsdkidl/WMT_PROXY_SETTING_NONE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WMT_PROXY_SETTINGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WMT_PROXY_SETTINGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

