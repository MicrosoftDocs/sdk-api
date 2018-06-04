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

# WSManProxyAccessType enumeration


## -description


Defines the proxy access type.


## -enum-fields




### -field WSMAN_OPTION_PROXY_IE_PROXY_CONFIG

Use the Internet Explorer proxy configuration for the current user. This is the default setting.


### -field WSMAN_OPTION_PROXY_WINHTTP_PROXY_CONFIG

Use the proxy settings configured for WinHTTP.


### -field WSMAN_OPTION_PROXY_AUTO_DETECT

Force autodetection of a proxy.


### -field WSMAN_OPTION_PROXY_NO_PROXY_SERVER

Do not use a proxy server. All host names are resolved locally.


## -remarks



The <b>WSMAN_OPTION_PROXY_IE_PROXY_CONFIG</b> option returns the current user Internet Explorer proxy settings for the current active network connection. This option requires the user profile to be loaded. This option can be directly used when called within a process that is running under an interactive user account identity. If the client application is running under a user context that is different than the interactive user, the client application must explicitly load the user profile prior to using this option.

If the Windows Remote Management API is called from a service,  <b>WSMAN_OPTION_PROXY_WINHTTP_PROXY_CONFIG</b> or <b>WSMAN_OPTION_PROXY_AUTO_DETECT</b> should be used if a proxy is required.

The <b>WSMAN_OPTION_PROXY_WINHTTP_PROXY_CONFIG</b> option translates into the <b>WINHTTP_ACCESS_TYPE_DEFAULT_PROXY</b> option in WinHTTP. WinHTTP retrieves the static proxy or direct configuration from the registry. <b>WINHTTP_ACCESS_TYPE_DEFAULT_PROXY</b> does not inherit browser proxy settings. WinHTTP does not share any proxy settings with Internet Explorer. This option gets the WinHTTP proxy configuration set by the ProxyCfg.exe utility.



