---
UID: NE:wsman.WSManProxyAccessType
title: WSManProxyAccessType (wsman.h)
description: Defines the proxy access type.
helpviewer_keywords: ["WSMAN_OPTION_PROXY_AUTO_DETECT","WSMAN_OPTION_PROXY_IE_PROXY_CONFIG","WSMAN_OPTION_PROXY_NO_PROXY_SERVER","WSMAN_OPTION_PROXY_WINHTTP_PROXY_CONFIG","WSManProxyAccessType","WSManProxyAccessType enumeration [Windows Remote Management]","winrm.wsmanproxyaccesstype","wsman/WSMAN_OPTION_PROXY_AUTO_DETECT","wsman/WSMAN_OPTION_PROXY_IE_PROXY_CONFIG","wsman/WSMAN_OPTION_PROXY_NO_PROXY_SERVER","wsman/WSMAN_OPTION_PROXY_WINHTTP_PROXY_CONFIG","wsman/WSManProxyAccessType"]
old-location: winrm\wsmanproxyaccesstype.htm
tech.root: winrm
ms.assetid: 0c7d13dc-42e0-4c91-bcdf-c198b557206b
ms.date: 12/05/2018
ms.keywords: WSMAN_OPTION_PROXY_AUTO_DETECT, WSMAN_OPTION_PROXY_IE_PROXY_CONFIG, WSMAN_OPTION_PROXY_NO_PROXY_SERVER, WSMAN_OPTION_PROXY_WINHTTP_PROXY_CONFIG, WSManProxyAccessType, WSManProxyAccessType enumeration [Windows Remote Management], winrm.wsmanproxyaccesstype, wsman/WSMAN_OPTION_PROXY_AUTO_DETECT, wsman/WSMAN_OPTION_PROXY_IE_PROXY_CONFIG, wsman/WSMAN_OPTION_PROXY_NO_PROXY_SERVER, wsman/WSMAN_OPTION_PROXY_WINHTTP_PROXY_CONFIG, wsman/WSManProxyAccessType
req.header: wsman.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
ms.custom: 19H1
f1_keywords:
 - WSManProxyAccessType
 - wsman/WSManProxyAccessType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wsman.h
api_name:
 - WSManProxyAccessType
---

# WSManProxyAccessType enumeration


## -description

Defines the proxy access type.

## -enum-fields

### -field WSMAN_OPTION_PROXY_IE_PROXY_CONFIG:1

Use the Internet Explorer proxy configuration for the current user. This is the default setting.

### -field WSMAN_OPTION_PROXY_WINHTTP_PROXY_CONFIG:2

Use the proxy settings configured for WinHTTP.

### -field WSMAN_OPTION_PROXY_AUTO_DETECT:4

Force autodetection of a proxy.

### -field WSMAN_OPTION_PROXY_NO_PROXY_SERVER:8

Do not use a proxy server. All host names are resolved locally.

## -remarks

The <b>WSMAN_OPTION_PROXY_IE_PROXY_CONFIG</b> option returns the current user Internet Explorer proxy settings for the current active network connection. This option requires the user profile to be loaded. This option can be directly used when called within a process that is running under an interactive user account identity. If the client application is running under a user context that is different than the interactive user, the client application must explicitly load the user profile prior to using this option.

If the Windows Remote Management API is called from a service,  <b>WSMAN_OPTION_PROXY_WINHTTP_PROXY_CONFIG</b> or <b>WSMAN_OPTION_PROXY_AUTO_DETECT</b> should be used if a proxy is required.

The <b>WSMAN_OPTION_PROXY_WINHTTP_PROXY_CONFIG</b> option translates into the <b>WINHTTP_ACCESS_TYPE_DEFAULT_PROXY</b> option in WinHTTP. WinHTTP retrieves the static proxy or direct configuration from the registry. <b>WINHTTP_ACCESS_TYPE_DEFAULT_PROXY</b> does not inherit browser proxy settings. WinHTTP does not share any proxy settings with Internet Explorer. This option gets the WinHTTP proxy configuration set by the ProxyCfg.exe utility.

